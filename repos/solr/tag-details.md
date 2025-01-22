<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `solr`

-	[`solr:8`](#solr8)
-	[`solr:8-slim`](#solr8-slim)
-	[`solr:8.11`](#solr811)
-	[`solr:8.11-slim`](#solr811-slim)
-	[`solr:8.11.4`](#solr8114)
-	[`solr:8.11.4-slim`](#solr8114-slim)
-	[`solr:9`](#solr9)
-	[`solr:9-slim`](#solr9-slim)
-	[`solr:9.7`](#solr97)
-	[`solr:9.7-slim`](#solr97-slim)
-	[`solr:9.7.0`](#solr970)
-	[`solr:9.7.0-slim`](#solr970-slim)
-	[`solr:9.8`](#solr98)
-	[`solr:9.8-slim`](#solr98-slim)
-	[`solr:9.8.0`](#solr980)
-	[`solr:9.8.0-slim`](#solr980-slim)
-	[`solr:latest`](#solrlatest)
-	[`solr:slim`](#solrslim)

## `solr:8`

```console
$ docker pull solr@sha256:7c0637b15c692cb03f95b72630c290cf6b1365b88789e3258ad09f3e0206cf01
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

### `solr:8` - linux; amd64

```console
$ docker pull solr@sha256:887a8fcff7abdbd125fb38f7f8e7e95ab4814d319185960cb80354574d664f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321760848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df7be3d13a6c5c109216572d0dde91725df512bc44fb927157b9b09a0ce6e76`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:7d20d76f38ebab7d6e8772ebb441099849fc90618b045e32662ead22b18506b6`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 20.3 MB (20256484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a591e2c0df0bf051ccca3642da020784df08274071ed8937da6f15ae417c7ff0`  
		Last Modified: Thu, 24 Oct 2024 00:57:04 GMT  
		Size: 47.2 MB (47215796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b5b5889414ee623c1071c8e3c220e569d98879ca753b5668ebc6d8166b7f1`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc2b98584a7dea2f5a034e7e0a40e289c9cf15ad8a985889a3c9955370af777`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6327c0d4759f72873bfa9d1358586f0fcd48f0977796b3c08561bcacee2e3fd`  
		Last Modified: Thu, 24 Oct 2024 02:00:01 GMT  
		Size: 1.3 MB (1347564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a85ab273c914a7fa42ef91ffe46e775fa4dd6d18f40488d4a973485abd3d41`  
		Last Modified: Thu, 24 Oct 2024 02:00:00 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fa4b5cbc0ddaa868f649d289b8285f3601d9cad3d1071b456a899a95e9ba2f`  
		Last Modified: Thu, 24 Oct 2024 02:00:00 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb952817a77f4e43af9d1a0132c871377f0ba0e9df730a5e089adbffb1c881db`  
		Last Modified: Thu, 24 Oct 2024 02:00:04 GMT  
		Size: 225.4 MB (225414034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77042038c8d5752027da05f3df8ef3ae3a1cae9ba767db0b5d5724f566e56d0`  
		Last Modified: Thu, 24 Oct 2024 02:00:01 GMT  
		Size: 6.3 KB (6277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8` - unknown; unknown

```console
$ docker pull solr@sha256:1495cb49effead0e396b7197b43d7b5e1905371de7b78aff5bbe26d25602cd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b20128679d1ab375b00bf5e970d9777f10b6882fe05e68520c8ffb2521f3d7`

```dockerfile
```

-	Layers:
	-	`sha256:3a6a31725159729836ced06316fdcd9d1a178bcfb36737809d6616938987066c`  
		Last Modified: Thu, 24 Oct 2024 02:00:00 GMT  
		Size: 4.2 MB (4202708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618db3d0a0ae3d10c8308b2a74ea40185429f9b5fddd0491ca3462772d31e3ed`  
		Last Modified: Thu, 24 Oct 2024 02:00:00 GMT  
		Size: 36.3 KB (36302 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:de6d899336cca171187cc2ed3000f1d3466b82265c75e49e9290fe6554c7e342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318285342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd14db2f788a9a528e336c21aa07884e5791c04d50a61a4b740ad1f045dadc0`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:7944fa14982850a5d6fef396e75bb75cff1a66cd0eb74db10ed75ba31d11c024`  
		Last Modified: Thu, 24 Oct 2024 00:56:58 GMT  
		Size: 20.1 MB (20093942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8d51799e7a038cc10554ed7b04e5a902ee5e6b3ca315d726100382293a207d`  
		Last Modified: Thu, 24 Oct 2024 01:05:49 GMT  
		Size: 45.6 MB (45578850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32b0317d30777fb74a12a1353e97c830b5d2c85173c5ce3d417606ee53f66b9`  
		Last Modified: Thu, 24 Oct 2024 01:05:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea45e6dcfef2a2e83c7d7129156bcf81ed16f6d0344688a9374f5edae650faa`  
		Last Modified: Thu, 24 Oct 2024 01:05:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a93c6587b99615c5452533b16110cc35a0b228fb484d9363dcf7f2fe6f747bc`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 1.2 MB (1208782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88ff62ec7ed8c16bdc5e0b00a4fe4437ceed6267698305153819d4fb178d83`  
		Last Modified: Thu, 24 Oct 2024 04:00:31 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79742506978e4173ef17d8e9f4d7c6f044d1ab7fd0a494490d7c8ca2816c3336`  
		Last Modified: Thu, 24 Oct 2024 04:00:31 GMT  
		Size: 2.9 KB (2886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e077ec63fb5f0d50a964253e0aaf9e626ec6ea86a261db70456f651c460a0a`  
		Last Modified: Thu, 24 Oct 2024 04:00:36 GMT  
		Size: 225.4 MB (225413995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fa310b208c6853fb3e2cbebd061788344aa5be9073ef26353f0f1ea88d218e`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8` - unknown; unknown

```console
$ docker pull solr@sha256:b3851a9cea4b521c02c14b01ccd1bfa4b07f37605d46334f045164e59f92d23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee03c928073697316eea28b4f2b9da80d21ab8f81fa77a943e79d9f94b4ef897`

```dockerfile
```

-	Layers:
	-	`sha256:03c5534f4b31202957bcfc572e92a95abe96b1098797919488dea67c5026f7fe`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 4.2 MB (4202974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:016fe4136b4ee1af5a3119b575e8d53c069ab76746adb091fb70dc3b98f07ac3`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 36.4 KB (36439 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8` - linux; ppc64le

```console
$ docker pull solr@sha256:5ef3ee425d7ca037c32b7568100acb8c3f5e002948e0f3eac1434beabc9463cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323970061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb30600293f781c0afb58de3ec604e2890eb8d02427b7d7cd96d815222d7636d`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:80f77674583b715acfc520100d8d6868a767a5eb5d74c71bcd1f0883576efdcc`  
		Last Modified: Thu, 24 Oct 2024 00:57:23 GMT  
		Size: 22.4 MB (22419063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d03d74ff88d2ffb8e137652aa420d18b78cbc7e797df869f022b5394ce25fbc`  
		Last Modified: Thu, 24 Oct 2024 08:54:43 GMT  
		Size: 42.7 MB (42675837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255a93f0295a15efbf9dd66f1ecb440214a5af14ce708721aa73305613b26d1d`  
		Last Modified: Thu, 24 Oct 2024 08:54:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ac21355d98d2bfa345f43721d74fc775131a4ca4586d96ebb78dd439cccb84`  
		Last Modified: Thu, 24 Oct 2024 08:54:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4b37e8f05c0fffca57485f3694efc9ff2f388b7251f73cc5eee74c8ff5b1f7`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 1.4 MB (1368761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c55b7efc496b3297c1c3f1a221b0d6099cbe673f37ec11bc15cfdd94a76adb`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134dbf31968e85e10cefbeba8261a869f4e85a02190de1b38d58a34d726ce555`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 2.9 KB (2886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cd8b364511cfb2e728aaf11d8a24686bc84ee37cfbb935dbc32d446047816c`  
		Last Modified: Thu, 24 Oct 2024 12:59:17 GMT  
		Size: 225.4 MB (225413985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21a93b838ea428cf3a706762741314b9656a0bd082ad1a266d492fd15e9eade`  
		Last Modified: Thu, 24 Oct 2024 12:59:10 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8` - unknown; unknown

```console
$ docker pull solr@sha256:9c818a08fea5946d7f770238b832483360a06ef4ebb7e8b8ec978afbbe06751d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c97e9e8130bf05c3053f69c60766f06abd5fbdddb4362ef6d776ef914e35b9`

```dockerfile
```

-	Layers:
	-	`sha256:05fb60499f0c1ddfff47f7a9a44aa230cda729b999f4476b3847a9d6d9d1eee5`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 4.2 MB (4206588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d13521967238eac2df0106af2f7f93299c681b62c44ea81604378bd0572b94b`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 36.3 KB (36346 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8` - linux; s390x

```console
$ docker pull solr@sha256:12d61ca229aa1f0c39725d2efef1300544b00e4fd160f758f2e0d6de4da1301e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313800413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b373c520228a2f61a57100e79a7ef045772b0ce691f3aabbb8ba547a1b8d6592`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:1229ca6c28b3587bf0822f628b9bc384d271a9e038f92df5c33bc243381ce251`  
		Last Modified: Thu, 24 Oct 2024 17:01:47 GMT  
		Size: 19.9 MB (19901078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d83916e7436ca079be5bb8b176191c09810a1fa36c2f06358b02fb1f6802b99`  
		Last Modified: Thu, 24 Oct 2024 17:11:08 GMT  
		Size: 40.8 MB (40841052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b7dcaca00531036656cc304d5476f74c8323f1c8e3f4743ce5235e0fdd55d2`  
		Last Modified: Thu, 24 Oct 2024 17:11:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51ba77675b0eb3c1b1844ba5cd4fd34b64ab5c469edd5af9aba5b3bf4edc66f`  
		Last Modified: Thu, 24 Oct 2024 17:11:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae259460cfaa0de12c65913b20c68b0cb5230fc3467929938634d56e490f83`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 1.3 MB (1262402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b300fd74f8a8451d028500b644bf64bd64a0aa87703ba6368e1d5ad7f08cf18`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88011dd25c8766c14bfdf6c25002502269ee0c1c425bef3195eb7d0f9646c36`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa4d44625483f3b7382abecba1606697dce3c8fda629b79325964e2f8fe38c`  
		Last Modified: Thu, 24 Oct 2024 19:33:09 GMT  
		Size: 225.4 MB (225413951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9f324b0d80fb4d063229afe3fa790b7467d4bf437d742063a4f4e452d37c48`  
		Last Modified: Thu, 24 Oct 2024 19:33:05 GMT  
		Size: 6.3 KB (6278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8` - unknown; unknown

```console
$ docker pull solr@sha256:765fda8116d009f24de81f0f9f2354986ffdc5204834d1d7eee6e0d91c53f6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a480c55889c341fb5c31b3639610c2daaf62a6c77927788833a629e585ae8316`

```dockerfile
```

-	Layers:
	-	`sha256:28ade2f994a3d1d95ba6be1b5f8c79ca82b2b5c606f63184e4725a1877643967`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 4.2 MB (4203508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:227a69c4aeae8da71f7df8183651c8adb2c777c21914a3c6733f34df6febf1ce`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 36.3 KB (36301 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:8-slim`

```console
$ docker pull solr@sha256:9a7261384b426f5c56cb4fefc561c37519db3e9ad47de9117ed84a5d6045d2d9
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
$ docker pull solr@sha256:8aaf66899e26a3fee17d0194ce362ecfe92bdb53ab43a50b2e67fe8c02f0bfa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321760829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7fb48128545e13b9321d50f87dc3183d729ffe054b650770ab0904e18cc5ea8`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:7d20d76f38ebab7d6e8772ebb441099849fc90618b045e32662ead22b18506b6`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 20.3 MB (20256484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a591e2c0df0bf051ccca3642da020784df08274071ed8937da6f15ae417c7ff0`  
		Last Modified: Thu, 24 Oct 2024 00:57:04 GMT  
		Size: 47.2 MB (47215796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b5b5889414ee623c1071c8e3c220e569d98879ca753b5668ebc6d8166b7f1`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc2b98584a7dea2f5a034e7e0a40e289c9cf15ad8a985889a3c9955370af777`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b255375c2870cc9d86fb55311f8e54fc5a00025126d8818ab9988f389166b56`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 1.3 MB (1347578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e414414823246d3bc84e6a3f7d598cadb87bac9c1096cb10d448f220e47b2a`  
		Last Modified: Thu, 24 Oct 2024 02:00:21 GMT  
		Size: 4.3 KB (4271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f75ce46ab1a97be1e6bf3db13a616dae1754795882fa932278d9e21af4a14c3`  
		Last Modified: Thu, 24 Oct 2024 02:00:21 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cfd760eb7f0355e78e0891f5395e13ebe98378087736a2d3714bf2bcdc8323`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 225.4 MB (225414009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef14d28b523252e9ebd5debde454666f1d0fb949291da84be9bf1c0ed449fd7`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 6.3 KB (6272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:3a509c33e2c99e19f3a179ece5d62114483e8d8df6c51bcea310b7c7a0c7c080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958e897fb45a6ec20bcb8113099ee387f663093e10d95187073a0766604bd316`

```dockerfile
```

-	Layers:
	-	`sha256:178edc135b5cb77ceecd00436bbab78d903f99d83aa6a6fd9a7cb3e26a318e5b`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 4.2 MB (4202738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92c474de06e24f9508f1b43a9be2aca1a7bbf54c268534546c33c61b1dd01e38`  
		Last Modified: Thu, 24 Oct 2024 02:00:21 GMT  
		Size: 36.4 KB (36351 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:d0db3fc1f8bba4dadf9e10eada3990b2bfa79bcfb241c831335c0890c1377239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318285342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd14db2f788a9a528e336c21aa07884e5791c04d50a61a4b740ad1f045dadc0`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:7944fa14982850a5d6fef396e75bb75cff1a66cd0eb74db10ed75ba31d11c024`  
		Last Modified: Thu, 24 Oct 2024 00:56:58 GMT  
		Size: 20.1 MB (20093942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8d51799e7a038cc10554ed7b04e5a902ee5e6b3ca315d726100382293a207d`  
		Last Modified: Thu, 24 Oct 2024 01:05:49 GMT  
		Size: 45.6 MB (45578850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32b0317d30777fb74a12a1353e97c830b5d2c85173c5ce3d417606ee53f66b9`  
		Last Modified: Thu, 24 Oct 2024 01:05:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea45e6dcfef2a2e83c7d7129156bcf81ed16f6d0344688a9374f5edae650faa`  
		Last Modified: Thu, 24 Oct 2024 01:05:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a93c6587b99615c5452533b16110cc35a0b228fb484d9363dcf7f2fe6f747bc`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 1.2 MB (1208782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88ff62ec7ed8c16bdc5e0b00a4fe4437ceed6267698305153819d4fb178d83`  
		Last Modified: Thu, 24 Oct 2024 04:00:31 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79742506978e4173ef17d8e9f4d7c6f044d1ab7fd0a494490d7c8ca2816c3336`  
		Last Modified: Thu, 24 Oct 2024 04:00:31 GMT  
		Size: 2.9 KB (2886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e077ec63fb5f0d50a964253e0aaf9e626ec6ea86a261db70456f651c460a0a`  
		Last Modified: Thu, 24 Oct 2024 04:00:36 GMT  
		Size: 225.4 MB (225413995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fa310b208c6853fb3e2cbebd061788344aa5be9073ef26353f0f1ea88d218e`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:8ce1cd9c8a77d09cf18cecb6150d2e418177b2159f163f1f596b4aed7391fe7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f12f1b56a2b85b7273c51c33afa700f0976dd5c4d1320f70762f2b2cf17990`

```dockerfile
```

-	Layers:
	-	`sha256:19f3b28182fcfe6090e6c3851f2324771457dea2ce1469afb09cfd9cd738ec86`  
		Last Modified: Thu, 24 Oct 2024 04:00:54 GMT  
		Size: 4.2 MB (4203004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63962b05a3836c789c1e691810d6d08c520387cade06a4f11dd05f9850647f3d`  
		Last Modified: Thu, 24 Oct 2024 04:00:53 GMT  
		Size: 36.5 KB (36488 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:130baa810e416b55581e7ef4f9dd5ad5f9a1459106c4495294d7c881d5a408b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323970061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb30600293f781c0afb58de3ec604e2890eb8d02427b7d7cd96d815222d7636d`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:80f77674583b715acfc520100d8d6868a767a5eb5d74c71bcd1f0883576efdcc`  
		Last Modified: Thu, 24 Oct 2024 00:57:23 GMT  
		Size: 22.4 MB (22419063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d03d74ff88d2ffb8e137652aa420d18b78cbc7e797df869f022b5394ce25fbc`  
		Last Modified: Thu, 24 Oct 2024 08:54:43 GMT  
		Size: 42.7 MB (42675837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255a93f0295a15efbf9dd66f1ecb440214a5af14ce708721aa73305613b26d1d`  
		Last Modified: Thu, 24 Oct 2024 08:54:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ac21355d98d2bfa345f43721d74fc775131a4ca4586d96ebb78dd439cccb84`  
		Last Modified: Thu, 24 Oct 2024 08:54:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4b37e8f05c0fffca57485f3694efc9ff2f388b7251f73cc5eee74c8ff5b1f7`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 1.4 MB (1368761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c55b7efc496b3297c1c3f1a221b0d6099cbe673f37ec11bc15cfdd94a76adb`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134dbf31968e85e10cefbeba8261a869f4e85a02190de1b38d58a34d726ce555`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 2.9 KB (2886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cd8b364511cfb2e728aaf11d8a24686bc84ee37cfbb935dbc32d446047816c`  
		Last Modified: Thu, 24 Oct 2024 12:59:17 GMT  
		Size: 225.4 MB (225413985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21a93b838ea428cf3a706762741314b9656a0bd082ad1a266d492fd15e9eade`  
		Last Modified: Thu, 24 Oct 2024 12:59:10 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:ef252ae6436e8be590f4d88edf1fa3bfe8f52988f2fa89eec1f0b81ef8f56273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4243013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830a4745894f75c1962f2d9b36b9ab7c477aad038a697ccdb5891fb8497a4aab`

```dockerfile
```

-	Layers:
	-	`sha256:5dd3297bd695aea00068eb70037e12f49d20efd8f773e372cdcd54ec5f697de0`  
		Last Modified: Thu, 24 Oct 2024 13:02:21 GMT  
		Size: 4.2 MB (4206618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba2c27f60d372f06a9012c60d0a90e3dae50f4162ce95d6ab218b0faab127b84`  
		Last Modified: Thu, 24 Oct 2024 13:02:20 GMT  
		Size: 36.4 KB (36395 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; s390x

```console
$ docker pull solr@sha256:2f9ac9a21127879330950419fdb676736ddf22e1d016c0f7e937d2e09c9c6d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313800413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b373c520228a2f61a57100e79a7ef045772b0ce691f3aabbb8ba547a1b8d6592`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:1229ca6c28b3587bf0822f628b9bc384d271a9e038f92df5c33bc243381ce251`  
		Last Modified: Thu, 24 Oct 2024 17:01:47 GMT  
		Size: 19.9 MB (19901078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d83916e7436ca079be5bb8b176191c09810a1fa36c2f06358b02fb1f6802b99`  
		Last Modified: Thu, 24 Oct 2024 17:11:08 GMT  
		Size: 40.8 MB (40841052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b7dcaca00531036656cc304d5476f74c8323f1c8e3f4743ce5235e0fdd55d2`  
		Last Modified: Thu, 24 Oct 2024 17:11:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51ba77675b0eb3c1b1844ba5cd4fd34b64ab5c469edd5af9aba5b3bf4edc66f`  
		Last Modified: Thu, 24 Oct 2024 17:11:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae259460cfaa0de12c65913b20c68b0cb5230fc3467929938634d56e490f83`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 1.3 MB (1262402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b300fd74f8a8451d028500b644bf64bd64a0aa87703ba6368e1d5ad7f08cf18`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88011dd25c8766c14bfdf6c25002502269ee0c1c425bef3195eb7d0f9646c36`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa4d44625483f3b7382abecba1606697dce3c8fda629b79325964e2f8fe38c`  
		Last Modified: Thu, 24 Oct 2024 19:33:09 GMT  
		Size: 225.4 MB (225413951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9f324b0d80fb4d063229afe3fa790b7467d4bf437d742063a4f4e452d37c48`  
		Last Modified: Thu, 24 Oct 2024 19:33:05 GMT  
		Size: 6.3 KB (6278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:5bb4dbfa837f94774fd6ee7742e552f950def16e950fb2c0eedfb6282db7d806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea11347c72f6438f9bb72d09755dcdfbdb96287a6700f89e0dd270e74fbb91c4`

```dockerfile
```

-	Layers:
	-	`sha256:528d371659b7335b9a8fcc40b18646d8d03e9b633463759c38d974714551d59a`  
		Last Modified: Thu, 24 Oct 2024 19:37:58 GMT  
		Size: 4.2 MB (4203538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed726a67b0a215795060e0e65ffeb7c0a6b8414a62889e3f4139117923a2cd87`  
		Last Modified: Thu, 24 Oct 2024 19:37:57 GMT  
		Size: 36.4 KB (36351 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:8.11`

```console
$ docker pull solr@sha256:7c0637b15c692cb03f95b72630c290cf6b1365b88789e3258ad09f3e0206cf01
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

### `solr:8.11` - linux; amd64

```console
$ docker pull solr@sha256:887a8fcff7abdbd125fb38f7f8e7e95ab4814d319185960cb80354574d664f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321760848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df7be3d13a6c5c109216572d0dde91725df512bc44fb927157b9b09a0ce6e76`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:7d20d76f38ebab7d6e8772ebb441099849fc90618b045e32662ead22b18506b6`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 20.3 MB (20256484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a591e2c0df0bf051ccca3642da020784df08274071ed8937da6f15ae417c7ff0`  
		Last Modified: Thu, 24 Oct 2024 00:57:04 GMT  
		Size: 47.2 MB (47215796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b5b5889414ee623c1071c8e3c220e569d98879ca753b5668ebc6d8166b7f1`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc2b98584a7dea2f5a034e7e0a40e289c9cf15ad8a985889a3c9955370af777`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6327c0d4759f72873bfa9d1358586f0fcd48f0977796b3c08561bcacee2e3fd`  
		Last Modified: Thu, 24 Oct 2024 02:00:01 GMT  
		Size: 1.3 MB (1347564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a85ab273c914a7fa42ef91ffe46e775fa4dd6d18f40488d4a973485abd3d41`  
		Last Modified: Thu, 24 Oct 2024 02:00:00 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fa4b5cbc0ddaa868f649d289b8285f3601d9cad3d1071b456a899a95e9ba2f`  
		Last Modified: Thu, 24 Oct 2024 02:00:00 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb952817a77f4e43af9d1a0132c871377f0ba0e9df730a5e089adbffb1c881db`  
		Last Modified: Thu, 24 Oct 2024 02:00:04 GMT  
		Size: 225.4 MB (225414034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77042038c8d5752027da05f3df8ef3ae3a1cae9ba767db0b5d5724f566e56d0`  
		Last Modified: Thu, 24 Oct 2024 02:00:01 GMT  
		Size: 6.3 KB (6277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11` - unknown; unknown

```console
$ docker pull solr@sha256:1495cb49effead0e396b7197b43d7b5e1905371de7b78aff5bbe26d25602cd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b20128679d1ab375b00bf5e970d9777f10b6882fe05e68520c8ffb2521f3d7`

```dockerfile
```

-	Layers:
	-	`sha256:3a6a31725159729836ced06316fdcd9d1a178bcfb36737809d6616938987066c`  
		Last Modified: Thu, 24 Oct 2024 02:00:00 GMT  
		Size: 4.2 MB (4202708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618db3d0a0ae3d10c8308b2a74ea40185429f9b5fddd0491ca3462772d31e3ed`  
		Last Modified: Thu, 24 Oct 2024 02:00:00 GMT  
		Size: 36.3 KB (36302 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:de6d899336cca171187cc2ed3000f1d3466b82265c75e49e9290fe6554c7e342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318285342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd14db2f788a9a528e336c21aa07884e5791c04d50a61a4b740ad1f045dadc0`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:7944fa14982850a5d6fef396e75bb75cff1a66cd0eb74db10ed75ba31d11c024`  
		Last Modified: Thu, 24 Oct 2024 00:56:58 GMT  
		Size: 20.1 MB (20093942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8d51799e7a038cc10554ed7b04e5a902ee5e6b3ca315d726100382293a207d`  
		Last Modified: Thu, 24 Oct 2024 01:05:49 GMT  
		Size: 45.6 MB (45578850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32b0317d30777fb74a12a1353e97c830b5d2c85173c5ce3d417606ee53f66b9`  
		Last Modified: Thu, 24 Oct 2024 01:05:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea45e6dcfef2a2e83c7d7129156bcf81ed16f6d0344688a9374f5edae650faa`  
		Last Modified: Thu, 24 Oct 2024 01:05:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a93c6587b99615c5452533b16110cc35a0b228fb484d9363dcf7f2fe6f747bc`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 1.2 MB (1208782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88ff62ec7ed8c16bdc5e0b00a4fe4437ceed6267698305153819d4fb178d83`  
		Last Modified: Thu, 24 Oct 2024 04:00:31 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79742506978e4173ef17d8e9f4d7c6f044d1ab7fd0a494490d7c8ca2816c3336`  
		Last Modified: Thu, 24 Oct 2024 04:00:31 GMT  
		Size: 2.9 KB (2886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e077ec63fb5f0d50a964253e0aaf9e626ec6ea86a261db70456f651c460a0a`  
		Last Modified: Thu, 24 Oct 2024 04:00:36 GMT  
		Size: 225.4 MB (225413995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fa310b208c6853fb3e2cbebd061788344aa5be9073ef26353f0f1ea88d218e`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11` - unknown; unknown

```console
$ docker pull solr@sha256:b3851a9cea4b521c02c14b01ccd1bfa4b07f37605d46334f045164e59f92d23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee03c928073697316eea28b4f2b9da80d21ab8f81fa77a943e79d9f94b4ef897`

```dockerfile
```

-	Layers:
	-	`sha256:03c5534f4b31202957bcfc572e92a95abe96b1098797919488dea67c5026f7fe`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 4.2 MB (4202974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:016fe4136b4ee1af5a3119b575e8d53c069ab76746adb091fb70dc3b98f07ac3`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 36.4 KB (36439 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11` - linux; ppc64le

```console
$ docker pull solr@sha256:5ef3ee425d7ca037c32b7568100acb8c3f5e002948e0f3eac1434beabc9463cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323970061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb30600293f781c0afb58de3ec604e2890eb8d02427b7d7cd96d815222d7636d`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:80f77674583b715acfc520100d8d6868a767a5eb5d74c71bcd1f0883576efdcc`  
		Last Modified: Thu, 24 Oct 2024 00:57:23 GMT  
		Size: 22.4 MB (22419063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d03d74ff88d2ffb8e137652aa420d18b78cbc7e797df869f022b5394ce25fbc`  
		Last Modified: Thu, 24 Oct 2024 08:54:43 GMT  
		Size: 42.7 MB (42675837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255a93f0295a15efbf9dd66f1ecb440214a5af14ce708721aa73305613b26d1d`  
		Last Modified: Thu, 24 Oct 2024 08:54:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ac21355d98d2bfa345f43721d74fc775131a4ca4586d96ebb78dd439cccb84`  
		Last Modified: Thu, 24 Oct 2024 08:54:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4b37e8f05c0fffca57485f3694efc9ff2f388b7251f73cc5eee74c8ff5b1f7`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 1.4 MB (1368761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c55b7efc496b3297c1c3f1a221b0d6099cbe673f37ec11bc15cfdd94a76adb`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134dbf31968e85e10cefbeba8261a869f4e85a02190de1b38d58a34d726ce555`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 2.9 KB (2886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cd8b364511cfb2e728aaf11d8a24686bc84ee37cfbb935dbc32d446047816c`  
		Last Modified: Thu, 24 Oct 2024 12:59:17 GMT  
		Size: 225.4 MB (225413985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21a93b838ea428cf3a706762741314b9656a0bd082ad1a266d492fd15e9eade`  
		Last Modified: Thu, 24 Oct 2024 12:59:10 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11` - unknown; unknown

```console
$ docker pull solr@sha256:9c818a08fea5946d7f770238b832483360a06ef4ebb7e8b8ec978afbbe06751d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c97e9e8130bf05c3053f69c60766f06abd5fbdddb4362ef6d776ef914e35b9`

```dockerfile
```

-	Layers:
	-	`sha256:05fb60499f0c1ddfff47f7a9a44aa230cda729b999f4476b3847a9d6d9d1eee5`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 4.2 MB (4206588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d13521967238eac2df0106af2f7f93299c681b62c44ea81604378bd0572b94b`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 36.3 KB (36346 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11` - linux; s390x

```console
$ docker pull solr@sha256:12d61ca229aa1f0c39725d2efef1300544b00e4fd160f758f2e0d6de4da1301e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313800413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b373c520228a2f61a57100e79a7ef045772b0ce691f3aabbb8ba547a1b8d6592`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:1229ca6c28b3587bf0822f628b9bc384d271a9e038f92df5c33bc243381ce251`  
		Last Modified: Thu, 24 Oct 2024 17:01:47 GMT  
		Size: 19.9 MB (19901078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d83916e7436ca079be5bb8b176191c09810a1fa36c2f06358b02fb1f6802b99`  
		Last Modified: Thu, 24 Oct 2024 17:11:08 GMT  
		Size: 40.8 MB (40841052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b7dcaca00531036656cc304d5476f74c8323f1c8e3f4743ce5235e0fdd55d2`  
		Last Modified: Thu, 24 Oct 2024 17:11:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51ba77675b0eb3c1b1844ba5cd4fd34b64ab5c469edd5af9aba5b3bf4edc66f`  
		Last Modified: Thu, 24 Oct 2024 17:11:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae259460cfaa0de12c65913b20c68b0cb5230fc3467929938634d56e490f83`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 1.3 MB (1262402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b300fd74f8a8451d028500b644bf64bd64a0aa87703ba6368e1d5ad7f08cf18`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88011dd25c8766c14bfdf6c25002502269ee0c1c425bef3195eb7d0f9646c36`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa4d44625483f3b7382abecba1606697dce3c8fda629b79325964e2f8fe38c`  
		Last Modified: Thu, 24 Oct 2024 19:33:09 GMT  
		Size: 225.4 MB (225413951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9f324b0d80fb4d063229afe3fa790b7467d4bf437d742063a4f4e452d37c48`  
		Last Modified: Thu, 24 Oct 2024 19:33:05 GMT  
		Size: 6.3 KB (6278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11` - unknown; unknown

```console
$ docker pull solr@sha256:765fda8116d009f24de81f0f9f2354986ffdc5204834d1d7eee6e0d91c53f6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a480c55889c341fb5c31b3639610c2daaf62a6c77927788833a629e585ae8316`

```dockerfile
```

-	Layers:
	-	`sha256:28ade2f994a3d1d95ba6be1b5f8c79ca82b2b5c606f63184e4725a1877643967`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 4.2 MB (4203508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:227a69c4aeae8da71f7df8183651c8adb2c777c21914a3c6733f34df6febf1ce`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 36.3 KB (36301 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:8.11-slim`

```console
$ docker pull solr@sha256:9a7261384b426f5c56cb4fefc561c37519db3e9ad47de9117ed84a5d6045d2d9
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

### `solr:8.11-slim` - linux; amd64

```console
$ docker pull solr@sha256:8aaf66899e26a3fee17d0194ce362ecfe92bdb53ab43a50b2e67fe8c02f0bfa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321760829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7fb48128545e13b9321d50f87dc3183d729ffe054b650770ab0904e18cc5ea8`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:7d20d76f38ebab7d6e8772ebb441099849fc90618b045e32662ead22b18506b6`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 20.3 MB (20256484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a591e2c0df0bf051ccca3642da020784df08274071ed8937da6f15ae417c7ff0`  
		Last Modified: Thu, 24 Oct 2024 00:57:04 GMT  
		Size: 47.2 MB (47215796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b5b5889414ee623c1071c8e3c220e569d98879ca753b5668ebc6d8166b7f1`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc2b98584a7dea2f5a034e7e0a40e289c9cf15ad8a985889a3c9955370af777`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b255375c2870cc9d86fb55311f8e54fc5a00025126d8818ab9988f389166b56`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 1.3 MB (1347578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e414414823246d3bc84e6a3f7d598cadb87bac9c1096cb10d448f220e47b2a`  
		Last Modified: Thu, 24 Oct 2024 02:00:21 GMT  
		Size: 4.3 KB (4271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f75ce46ab1a97be1e6bf3db13a616dae1754795882fa932278d9e21af4a14c3`  
		Last Modified: Thu, 24 Oct 2024 02:00:21 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cfd760eb7f0355e78e0891f5395e13ebe98378087736a2d3714bf2bcdc8323`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 225.4 MB (225414009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef14d28b523252e9ebd5debde454666f1d0fb949291da84be9bf1c0ed449fd7`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 6.3 KB (6272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11-slim` - unknown; unknown

```console
$ docker pull solr@sha256:3a509c33e2c99e19f3a179ece5d62114483e8d8df6c51bcea310b7c7a0c7c080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958e897fb45a6ec20bcb8113099ee387f663093e10d95187073a0766604bd316`

```dockerfile
```

-	Layers:
	-	`sha256:178edc135b5cb77ceecd00436bbab78d903f99d83aa6a6fd9a7cb3e26a318e5b`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 4.2 MB (4202738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92c474de06e24f9508f1b43a9be2aca1a7bbf54c268534546c33c61b1dd01e38`  
		Last Modified: Thu, 24 Oct 2024 02:00:21 GMT  
		Size: 36.4 KB (36351 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:d0db3fc1f8bba4dadf9e10eada3990b2bfa79bcfb241c831335c0890c1377239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318285342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd14db2f788a9a528e336c21aa07884e5791c04d50a61a4b740ad1f045dadc0`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:7944fa14982850a5d6fef396e75bb75cff1a66cd0eb74db10ed75ba31d11c024`  
		Last Modified: Thu, 24 Oct 2024 00:56:58 GMT  
		Size: 20.1 MB (20093942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8d51799e7a038cc10554ed7b04e5a902ee5e6b3ca315d726100382293a207d`  
		Last Modified: Thu, 24 Oct 2024 01:05:49 GMT  
		Size: 45.6 MB (45578850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32b0317d30777fb74a12a1353e97c830b5d2c85173c5ce3d417606ee53f66b9`  
		Last Modified: Thu, 24 Oct 2024 01:05:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea45e6dcfef2a2e83c7d7129156bcf81ed16f6d0344688a9374f5edae650faa`  
		Last Modified: Thu, 24 Oct 2024 01:05:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a93c6587b99615c5452533b16110cc35a0b228fb484d9363dcf7f2fe6f747bc`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 1.2 MB (1208782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88ff62ec7ed8c16bdc5e0b00a4fe4437ceed6267698305153819d4fb178d83`  
		Last Modified: Thu, 24 Oct 2024 04:00:31 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79742506978e4173ef17d8e9f4d7c6f044d1ab7fd0a494490d7c8ca2816c3336`  
		Last Modified: Thu, 24 Oct 2024 04:00:31 GMT  
		Size: 2.9 KB (2886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e077ec63fb5f0d50a964253e0aaf9e626ec6ea86a261db70456f651c460a0a`  
		Last Modified: Thu, 24 Oct 2024 04:00:36 GMT  
		Size: 225.4 MB (225413995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fa310b208c6853fb3e2cbebd061788344aa5be9073ef26353f0f1ea88d218e`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11-slim` - unknown; unknown

```console
$ docker pull solr@sha256:8ce1cd9c8a77d09cf18cecb6150d2e418177b2159f163f1f596b4aed7391fe7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f12f1b56a2b85b7273c51c33afa700f0976dd5c4d1320f70762f2b2cf17990`

```dockerfile
```

-	Layers:
	-	`sha256:19f3b28182fcfe6090e6c3851f2324771457dea2ce1469afb09cfd9cd738ec86`  
		Last Modified: Thu, 24 Oct 2024 04:00:54 GMT  
		Size: 4.2 MB (4203004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63962b05a3836c789c1e691810d6d08c520387cade06a4f11dd05f9850647f3d`  
		Last Modified: Thu, 24 Oct 2024 04:00:53 GMT  
		Size: 36.5 KB (36488 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:130baa810e416b55581e7ef4f9dd5ad5f9a1459106c4495294d7c881d5a408b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323970061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb30600293f781c0afb58de3ec604e2890eb8d02427b7d7cd96d815222d7636d`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:80f77674583b715acfc520100d8d6868a767a5eb5d74c71bcd1f0883576efdcc`  
		Last Modified: Thu, 24 Oct 2024 00:57:23 GMT  
		Size: 22.4 MB (22419063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d03d74ff88d2ffb8e137652aa420d18b78cbc7e797df869f022b5394ce25fbc`  
		Last Modified: Thu, 24 Oct 2024 08:54:43 GMT  
		Size: 42.7 MB (42675837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255a93f0295a15efbf9dd66f1ecb440214a5af14ce708721aa73305613b26d1d`  
		Last Modified: Thu, 24 Oct 2024 08:54:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ac21355d98d2bfa345f43721d74fc775131a4ca4586d96ebb78dd439cccb84`  
		Last Modified: Thu, 24 Oct 2024 08:54:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4b37e8f05c0fffca57485f3694efc9ff2f388b7251f73cc5eee74c8ff5b1f7`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 1.4 MB (1368761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c55b7efc496b3297c1c3f1a221b0d6099cbe673f37ec11bc15cfdd94a76adb`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134dbf31968e85e10cefbeba8261a869f4e85a02190de1b38d58a34d726ce555`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 2.9 KB (2886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cd8b364511cfb2e728aaf11d8a24686bc84ee37cfbb935dbc32d446047816c`  
		Last Modified: Thu, 24 Oct 2024 12:59:17 GMT  
		Size: 225.4 MB (225413985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21a93b838ea428cf3a706762741314b9656a0bd082ad1a266d492fd15e9eade`  
		Last Modified: Thu, 24 Oct 2024 12:59:10 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11-slim` - unknown; unknown

```console
$ docker pull solr@sha256:ef252ae6436e8be590f4d88edf1fa3bfe8f52988f2fa89eec1f0b81ef8f56273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4243013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830a4745894f75c1962f2d9b36b9ab7c477aad038a697ccdb5891fb8497a4aab`

```dockerfile
```

-	Layers:
	-	`sha256:5dd3297bd695aea00068eb70037e12f49d20efd8f773e372cdcd54ec5f697de0`  
		Last Modified: Thu, 24 Oct 2024 13:02:21 GMT  
		Size: 4.2 MB (4206618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba2c27f60d372f06a9012c60d0a90e3dae50f4162ce95d6ab218b0faab127b84`  
		Last Modified: Thu, 24 Oct 2024 13:02:20 GMT  
		Size: 36.4 KB (36395 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11-slim` - linux; s390x

```console
$ docker pull solr@sha256:2f9ac9a21127879330950419fdb676736ddf22e1d016c0f7e937d2e09c9c6d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313800413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b373c520228a2f61a57100e79a7ef045772b0ce691f3aabbb8ba547a1b8d6592`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:1229ca6c28b3587bf0822f628b9bc384d271a9e038f92df5c33bc243381ce251`  
		Last Modified: Thu, 24 Oct 2024 17:01:47 GMT  
		Size: 19.9 MB (19901078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d83916e7436ca079be5bb8b176191c09810a1fa36c2f06358b02fb1f6802b99`  
		Last Modified: Thu, 24 Oct 2024 17:11:08 GMT  
		Size: 40.8 MB (40841052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b7dcaca00531036656cc304d5476f74c8323f1c8e3f4743ce5235e0fdd55d2`  
		Last Modified: Thu, 24 Oct 2024 17:11:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51ba77675b0eb3c1b1844ba5cd4fd34b64ab5c469edd5af9aba5b3bf4edc66f`  
		Last Modified: Thu, 24 Oct 2024 17:11:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae259460cfaa0de12c65913b20c68b0cb5230fc3467929938634d56e490f83`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 1.3 MB (1262402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b300fd74f8a8451d028500b644bf64bd64a0aa87703ba6368e1d5ad7f08cf18`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88011dd25c8766c14bfdf6c25002502269ee0c1c425bef3195eb7d0f9646c36`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa4d44625483f3b7382abecba1606697dce3c8fda629b79325964e2f8fe38c`  
		Last Modified: Thu, 24 Oct 2024 19:33:09 GMT  
		Size: 225.4 MB (225413951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9f324b0d80fb4d063229afe3fa790b7467d4bf437d742063a4f4e452d37c48`  
		Last Modified: Thu, 24 Oct 2024 19:33:05 GMT  
		Size: 6.3 KB (6278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11-slim` - unknown; unknown

```console
$ docker pull solr@sha256:5bb4dbfa837f94774fd6ee7742e552f950def16e950fb2c0eedfb6282db7d806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea11347c72f6438f9bb72d09755dcdfbdb96287a6700f89e0dd270e74fbb91c4`

```dockerfile
```

-	Layers:
	-	`sha256:528d371659b7335b9a8fcc40b18646d8d03e9b633463759c38d974714551d59a`  
		Last Modified: Thu, 24 Oct 2024 19:37:58 GMT  
		Size: 4.2 MB (4203538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed726a67b0a215795060e0e65ffeb7c0a6b8414a62889e3f4139117923a2cd87`  
		Last Modified: Thu, 24 Oct 2024 19:37:57 GMT  
		Size: 36.4 KB (36351 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:8.11.4`

```console
$ docker pull solr@sha256:7c0637b15c692cb03f95b72630c290cf6b1365b88789e3258ad09f3e0206cf01
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

### `solr:8.11.4` - linux; amd64

```console
$ docker pull solr@sha256:887a8fcff7abdbd125fb38f7f8e7e95ab4814d319185960cb80354574d664f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321760848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df7be3d13a6c5c109216572d0dde91725df512bc44fb927157b9b09a0ce6e76`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:7d20d76f38ebab7d6e8772ebb441099849fc90618b045e32662ead22b18506b6`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 20.3 MB (20256484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a591e2c0df0bf051ccca3642da020784df08274071ed8937da6f15ae417c7ff0`  
		Last Modified: Thu, 24 Oct 2024 00:57:04 GMT  
		Size: 47.2 MB (47215796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b5b5889414ee623c1071c8e3c220e569d98879ca753b5668ebc6d8166b7f1`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc2b98584a7dea2f5a034e7e0a40e289c9cf15ad8a985889a3c9955370af777`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6327c0d4759f72873bfa9d1358586f0fcd48f0977796b3c08561bcacee2e3fd`  
		Last Modified: Thu, 24 Oct 2024 02:00:01 GMT  
		Size: 1.3 MB (1347564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a85ab273c914a7fa42ef91ffe46e775fa4dd6d18f40488d4a973485abd3d41`  
		Last Modified: Thu, 24 Oct 2024 02:00:00 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fa4b5cbc0ddaa868f649d289b8285f3601d9cad3d1071b456a899a95e9ba2f`  
		Last Modified: Thu, 24 Oct 2024 02:00:00 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb952817a77f4e43af9d1a0132c871377f0ba0e9df730a5e089adbffb1c881db`  
		Last Modified: Thu, 24 Oct 2024 02:00:04 GMT  
		Size: 225.4 MB (225414034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77042038c8d5752027da05f3df8ef3ae3a1cae9ba767db0b5d5724f566e56d0`  
		Last Modified: Thu, 24 Oct 2024 02:00:01 GMT  
		Size: 6.3 KB (6277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11.4` - unknown; unknown

```console
$ docker pull solr@sha256:1495cb49effead0e396b7197b43d7b5e1905371de7b78aff5bbe26d25602cd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b20128679d1ab375b00bf5e970d9777f10b6882fe05e68520c8ffb2521f3d7`

```dockerfile
```

-	Layers:
	-	`sha256:3a6a31725159729836ced06316fdcd9d1a178bcfb36737809d6616938987066c`  
		Last Modified: Thu, 24 Oct 2024 02:00:00 GMT  
		Size: 4.2 MB (4202708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618db3d0a0ae3d10c8308b2a74ea40185429f9b5fddd0491ca3462772d31e3ed`  
		Last Modified: Thu, 24 Oct 2024 02:00:00 GMT  
		Size: 36.3 KB (36302 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11.4` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:de6d899336cca171187cc2ed3000f1d3466b82265c75e49e9290fe6554c7e342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318285342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd14db2f788a9a528e336c21aa07884e5791c04d50a61a4b740ad1f045dadc0`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:7944fa14982850a5d6fef396e75bb75cff1a66cd0eb74db10ed75ba31d11c024`  
		Last Modified: Thu, 24 Oct 2024 00:56:58 GMT  
		Size: 20.1 MB (20093942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8d51799e7a038cc10554ed7b04e5a902ee5e6b3ca315d726100382293a207d`  
		Last Modified: Thu, 24 Oct 2024 01:05:49 GMT  
		Size: 45.6 MB (45578850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32b0317d30777fb74a12a1353e97c830b5d2c85173c5ce3d417606ee53f66b9`  
		Last Modified: Thu, 24 Oct 2024 01:05:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea45e6dcfef2a2e83c7d7129156bcf81ed16f6d0344688a9374f5edae650faa`  
		Last Modified: Thu, 24 Oct 2024 01:05:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a93c6587b99615c5452533b16110cc35a0b228fb484d9363dcf7f2fe6f747bc`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 1.2 MB (1208782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88ff62ec7ed8c16bdc5e0b00a4fe4437ceed6267698305153819d4fb178d83`  
		Last Modified: Thu, 24 Oct 2024 04:00:31 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79742506978e4173ef17d8e9f4d7c6f044d1ab7fd0a494490d7c8ca2816c3336`  
		Last Modified: Thu, 24 Oct 2024 04:00:31 GMT  
		Size: 2.9 KB (2886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e077ec63fb5f0d50a964253e0aaf9e626ec6ea86a261db70456f651c460a0a`  
		Last Modified: Thu, 24 Oct 2024 04:00:36 GMT  
		Size: 225.4 MB (225413995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fa310b208c6853fb3e2cbebd061788344aa5be9073ef26353f0f1ea88d218e`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11.4` - unknown; unknown

```console
$ docker pull solr@sha256:b3851a9cea4b521c02c14b01ccd1bfa4b07f37605d46334f045164e59f92d23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee03c928073697316eea28b4f2b9da80d21ab8f81fa77a943e79d9f94b4ef897`

```dockerfile
```

-	Layers:
	-	`sha256:03c5534f4b31202957bcfc572e92a95abe96b1098797919488dea67c5026f7fe`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 4.2 MB (4202974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:016fe4136b4ee1af5a3119b575e8d53c069ab76746adb091fb70dc3b98f07ac3`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 36.4 KB (36439 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11.4` - linux; ppc64le

```console
$ docker pull solr@sha256:5ef3ee425d7ca037c32b7568100acb8c3f5e002948e0f3eac1434beabc9463cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323970061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb30600293f781c0afb58de3ec604e2890eb8d02427b7d7cd96d815222d7636d`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:80f77674583b715acfc520100d8d6868a767a5eb5d74c71bcd1f0883576efdcc`  
		Last Modified: Thu, 24 Oct 2024 00:57:23 GMT  
		Size: 22.4 MB (22419063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d03d74ff88d2ffb8e137652aa420d18b78cbc7e797df869f022b5394ce25fbc`  
		Last Modified: Thu, 24 Oct 2024 08:54:43 GMT  
		Size: 42.7 MB (42675837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255a93f0295a15efbf9dd66f1ecb440214a5af14ce708721aa73305613b26d1d`  
		Last Modified: Thu, 24 Oct 2024 08:54:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ac21355d98d2bfa345f43721d74fc775131a4ca4586d96ebb78dd439cccb84`  
		Last Modified: Thu, 24 Oct 2024 08:54:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4b37e8f05c0fffca57485f3694efc9ff2f388b7251f73cc5eee74c8ff5b1f7`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 1.4 MB (1368761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c55b7efc496b3297c1c3f1a221b0d6099cbe673f37ec11bc15cfdd94a76adb`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134dbf31968e85e10cefbeba8261a869f4e85a02190de1b38d58a34d726ce555`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 2.9 KB (2886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cd8b364511cfb2e728aaf11d8a24686bc84ee37cfbb935dbc32d446047816c`  
		Last Modified: Thu, 24 Oct 2024 12:59:17 GMT  
		Size: 225.4 MB (225413985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21a93b838ea428cf3a706762741314b9656a0bd082ad1a266d492fd15e9eade`  
		Last Modified: Thu, 24 Oct 2024 12:59:10 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11.4` - unknown; unknown

```console
$ docker pull solr@sha256:9c818a08fea5946d7f770238b832483360a06ef4ebb7e8b8ec978afbbe06751d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c97e9e8130bf05c3053f69c60766f06abd5fbdddb4362ef6d776ef914e35b9`

```dockerfile
```

-	Layers:
	-	`sha256:05fb60499f0c1ddfff47f7a9a44aa230cda729b999f4476b3847a9d6d9d1eee5`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 4.2 MB (4206588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d13521967238eac2df0106af2f7f93299c681b62c44ea81604378bd0572b94b`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 36.3 KB (36346 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11.4` - linux; s390x

```console
$ docker pull solr@sha256:12d61ca229aa1f0c39725d2efef1300544b00e4fd160f758f2e0d6de4da1301e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313800413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b373c520228a2f61a57100e79a7ef045772b0ce691f3aabbb8ba547a1b8d6592`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:1229ca6c28b3587bf0822f628b9bc384d271a9e038f92df5c33bc243381ce251`  
		Last Modified: Thu, 24 Oct 2024 17:01:47 GMT  
		Size: 19.9 MB (19901078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d83916e7436ca079be5bb8b176191c09810a1fa36c2f06358b02fb1f6802b99`  
		Last Modified: Thu, 24 Oct 2024 17:11:08 GMT  
		Size: 40.8 MB (40841052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b7dcaca00531036656cc304d5476f74c8323f1c8e3f4743ce5235e0fdd55d2`  
		Last Modified: Thu, 24 Oct 2024 17:11:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51ba77675b0eb3c1b1844ba5cd4fd34b64ab5c469edd5af9aba5b3bf4edc66f`  
		Last Modified: Thu, 24 Oct 2024 17:11:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae259460cfaa0de12c65913b20c68b0cb5230fc3467929938634d56e490f83`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 1.3 MB (1262402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b300fd74f8a8451d028500b644bf64bd64a0aa87703ba6368e1d5ad7f08cf18`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88011dd25c8766c14bfdf6c25002502269ee0c1c425bef3195eb7d0f9646c36`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa4d44625483f3b7382abecba1606697dce3c8fda629b79325964e2f8fe38c`  
		Last Modified: Thu, 24 Oct 2024 19:33:09 GMT  
		Size: 225.4 MB (225413951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9f324b0d80fb4d063229afe3fa790b7467d4bf437d742063a4f4e452d37c48`  
		Last Modified: Thu, 24 Oct 2024 19:33:05 GMT  
		Size: 6.3 KB (6278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11.4` - unknown; unknown

```console
$ docker pull solr@sha256:765fda8116d009f24de81f0f9f2354986ffdc5204834d1d7eee6e0d91c53f6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a480c55889c341fb5c31b3639610c2daaf62a6c77927788833a629e585ae8316`

```dockerfile
```

-	Layers:
	-	`sha256:28ade2f994a3d1d95ba6be1b5f8c79ca82b2b5c606f63184e4725a1877643967`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 4.2 MB (4203508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:227a69c4aeae8da71f7df8183651c8adb2c777c21914a3c6733f34df6febf1ce`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 36.3 KB (36301 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:8.11.4-slim`

```console
$ docker pull solr@sha256:9a7261384b426f5c56cb4fefc561c37519db3e9ad47de9117ed84a5d6045d2d9
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

### `solr:8.11.4-slim` - linux; amd64

```console
$ docker pull solr@sha256:8aaf66899e26a3fee17d0194ce362ecfe92bdb53ab43a50b2e67fe8c02f0bfa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321760829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7fb48128545e13b9321d50f87dc3183d729ffe054b650770ab0904e18cc5ea8`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:7d20d76f38ebab7d6e8772ebb441099849fc90618b045e32662ead22b18506b6`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 20.3 MB (20256484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a591e2c0df0bf051ccca3642da020784df08274071ed8937da6f15ae417c7ff0`  
		Last Modified: Thu, 24 Oct 2024 00:57:04 GMT  
		Size: 47.2 MB (47215796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b5b5889414ee623c1071c8e3c220e569d98879ca753b5668ebc6d8166b7f1`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc2b98584a7dea2f5a034e7e0a40e289c9cf15ad8a985889a3c9955370af777`  
		Last Modified: Thu, 24 Oct 2024 00:57:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b255375c2870cc9d86fb55311f8e54fc5a00025126d8818ab9988f389166b56`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 1.3 MB (1347578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e414414823246d3bc84e6a3f7d598cadb87bac9c1096cb10d448f220e47b2a`  
		Last Modified: Thu, 24 Oct 2024 02:00:21 GMT  
		Size: 4.3 KB (4271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f75ce46ab1a97be1e6bf3db13a616dae1754795882fa932278d9e21af4a14c3`  
		Last Modified: Thu, 24 Oct 2024 02:00:21 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cfd760eb7f0355e78e0891f5395e13ebe98378087736a2d3714bf2bcdc8323`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 225.4 MB (225414009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef14d28b523252e9ebd5debde454666f1d0fb949291da84be9bf1c0ed449fd7`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 6.3 KB (6272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11.4-slim` - unknown; unknown

```console
$ docker pull solr@sha256:3a509c33e2c99e19f3a179ece5d62114483e8d8df6c51bcea310b7c7a0c7c080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958e897fb45a6ec20bcb8113099ee387f663093e10d95187073a0766604bd316`

```dockerfile
```

-	Layers:
	-	`sha256:178edc135b5cb77ceecd00436bbab78d903f99d83aa6a6fd9a7cb3e26a318e5b`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 4.2 MB (4202738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92c474de06e24f9508f1b43a9be2aca1a7bbf54c268534546c33c61b1dd01e38`  
		Last Modified: Thu, 24 Oct 2024 02:00:21 GMT  
		Size: 36.4 KB (36351 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11.4-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:d0db3fc1f8bba4dadf9e10eada3990b2bfa79bcfb241c831335c0890c1377239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318285342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd14db2f788a9a528e336c21aa07884e5791c04d50a61a4b740ad1f045dadc0`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:7944fa14982850a5d6fef396e75bb75cff1a66cd0eb74db10ed75ba31d11c024`  
		Last Modified: Thu, 24 Oct 2024 00:56:58 GMT  
		Size: 20.1 MB (20093942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8d51799e7a038cc10554ed7b04e5a902ee5e6b3ca315d726100382293a207d`  
		Last Modified: Thu, 24 Oct 2024 01:05:49 GMT  
		Size: 45.6 MB (45578850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32b0317d30777fb74a12a1353e97c830b5d2c85173c5ce3d417606ee53f66b9`  
		Last Modified: Thu, 24 Oct 2024 01:05:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea45e6dcfef2a2e83c7d7129156bcf81ed16f6d0344688a9374f5edae650faa`  
		Last Modified: Thu, 24 Oct 2024 01:05:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a93c6587b99615c5452533b16110cc35a0b228fb484d9363dcf7f2fe6f747bc`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 1.2 MB (1208782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88ff62ec7ed8c16bdc5e0b00a4fe4437ceed6267698305153819d4fb178d83`  
		Last Modified: Thu, 24 Oct 2024 04:00:31 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79742506978e4173ef17d8e9f4d7c6f044d1ab7fd0a494490d7c8ca2816c3336`  
		Last Modified: Thu, 24 Oct 2024 04:00:31 GMT  
		Size: 2.9 KB (2886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e077ec63fb5f0d50a964253e0aaf9e626ec6ea86a261db70456f651c460a0a`  
		Last Modified: Thu, 24 Oct 2024 04:00:36 GMT  
		Size: 225.4 MB (225413995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fa310b208c6853fb3e2cbebd061788344aa5be9073ef26353f0f1ea88d218e`  
		Last Modified: Thu, 24 Oct 2024 04:00:32 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11.4-slim` - unknown; unknown

```console
$ docker pull solr@sha256:8ce1cd9c8a77d09cf18cecb6150d2e418177b2159f163f1f596b4aed7391fe7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f12f1b56a2b85b7273c51c33afa700f0976dd5c4d1320f70762f2b2cf17990`

```dockerfile
```

-	Layers:
	-	`sha256:19f3b28182fcfe6090e6c3851f2324771457dea2ce1469afb09cfd9cd738ec86`  
		Last Modified: Thu, 24 Oct 2024 04:00:54 GMT  
		Size: 4.2 MB (4203004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63962b05a3836c789c1e691810d6d08c520387cade06a4f11dd05f9850647f3d`  
		Last Modified: Thu, 24 Oct 2024 04:00:53 GMT  
		Size: 36.5 KB (36488 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11.4-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:130baa810e416b55581e7ef4f9dd5ad5f9a1459106c4495294d7c881d5a408b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323970061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb30600293f781c0afb58de3ec604e2890eb8d02427b7d7cd96d815222d7636d`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:80f77674583b715acfc520100d8d6868a767a5eb5d74c71bcd1f0883576efdcc`  
		Last Modified: Thu, 24 Oct 2024 00:57:23 GMT  
		Size: 22.4 MB (22419063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d03d74ff88d2ffb8e137652aa420d18b78cbc7e797df869f022b5394ce25fbc`  
		Last Modified: Thu, 24 Oct 2024 08:54:43 GMT  
		Size: 42.7 MB (42675837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255a93f0295a15efbf9dd66f1ecb440214a5af14ce708721aa73305613b26d1d`  
		Last Modified: Thu, 24 Oct 2024 08:54:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ac21355d98d2bfa345f43721d74fc775131a4ca4586d96ebb78dd439cccb84`  
		Last Modified: Thu, 24 Oct 2024 08:54:41 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4b37e8f05c0fffca57485f3694efc9ff2f388b7251f73cc5eee74c8ff5b1f7`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 1.4 MB (1368761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c55b7efc496b3297c1c3f1a221b0d6099cbe673f37ec11bc15cfdd94a76adb`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134dbf31968e85e10cefbeba8261a869f4e85a02190de1b38d58a34d726ce555`  
		Last Modified: Thu, 24 Oct 2024 12:59:09 GMT  
		Size: 2.9 KB (2886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cd8b364511cfb2e728aaf11d8a24686bc84ee37cfbb935dbc32d446047816c`  
		Last Modified: Thu, 24 Oct 2024 12:59:17 GMT  
		Size: 225.4 MB (225413985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21a93b838ea428cf3a706762741314b9656a0bd082ad1a266d492fd15e9eade`  
		Last Modified: Thu, 24 Oct 2024 12:59:10 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11.4-slim` - unknown; unknown

```console
$ docker pull solr@sha256:ef252ae6436e8be590f4d88edf1fa3bfe8f52988f2fa89eec1f0b81ef8f56273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4243013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830a4745894f75c1962f2d9b36b9ab7c477aad038a697ccdb5891fb8497a4aab`

```dockerfile
```

-	Layers:
	-	`sha256:5dd3297bd695aea00068eb70037e12f49d20efd8f773e372cdcd54ec5f697de0`  
		Last Modified: Thu, 24 Oct 2024 13:02:21 GMT  
		Size: 4.2 MB (4206618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba2c27f60d372f06a9012c60d0a90e3dae50f4162ce95d6ab218b0faab127b84`  
		Last Modified: Thu, 24 Oct 2024 13:02:20 GMT  
		Size: 36.4 KB (36395 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11.4-slim` - linux; s390x

```console
$ docker pull solr@sha256:2f9ac9a21127879330950419fdb676736ddf22e1d016c0f7e937d2e09c9c6d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313800413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b373c520228a2f61a57100e79a7ef045772b0ce691f3aabbb8ba547a1b8d6592`
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6b7b1297da762cf2b1eb4834073e6a45cda82a359efb17a89eba3fc6b59b4d26';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:1229ca6c28b3587bf0822f628b9bc384d271a9e038f92df5c33bc243381ce251`  
		Last Modified: Thu, 24 Oct 2024 17:01:47 GMT  
		Size: 19.9 MB (19901078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d83916e7436ca079be5bb8b176191c09810a1fa36c2f06358b02fb1f6802b99`  
		Last Modified: Thu, 24 Oct 2024 17:11:08 GMT  
		Size: 40.8 MB (40841052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b7dcaca00531036656cc304d5476f74c8323f1c8e3f4743ce5235e0fdd55d2`  
		Last Modified: Thu, 24 Oct 2024 17:11:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51ba77675b0eb3c1b1844ba5cd4fd34b64ab5c469edd5af9aba5b3bf4edc66f`  
		Last Modified: Thu, 24 Oct 2024 17:11:08 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae259460cfaa0de12c65913b20c68b0cb5230fc3467929938634d56e490f83`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 1.3 MB (1262402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b300fd74f8a8451d028500b644bf64bd64a0aa87703ba6368e1d5ad7f08cf18`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88011dd25c8766c14bfdf6c25002502269ee0c1c425bef3195eb7d0f9646c36`  
		Last Modified: Thu, 24 Oct 2024 19:33:04 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa4d44625483f3b7382abecba1606697dce3c8fda629b79325964e2f8fe38c`  
		Last Modified: Thu, 24 Oct 2024 19:33:09 GMT  
		Size: 225.4 MB (225413951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9f324b0d80fb4d063229afe3fa790b7467d4bf437d742063a4f4e452d37c48`  
		Last Modified: Thu, 24 Oct 2024 19:33:05 GMT  
		Size: 6.3 KB (6278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11.4-slim` - unknown; unknown

```console
$ docker pull solr@sha256:5bb4dbfa837f94774fd6ee7742e552f950def16e950fb2c0eedfb6282db7d806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea11347c72f6438f9bb72d09755dcdfbdb96287a6700f89e0dd270e74fbb91c4`

```dockerfile
```

-	Layers:
	-	`sha256:528d371659b7335b9a8fcc40b18646d8d03e9b633463759c38d974714551d59a`  
		Last Modified: Thu, 24 Oct 2024 19:37:58 GMT  
		Size: 4.2 MB (4203538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed726a67b0a215795060e0e65ffeb7c0a6b8414a62889e3f4139117923a2cd87`  
		Last Modified: Thu, 24 Oct 2024 19:37:57 GMT  
		Size: 36.4 KB (36351 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9`

```console
$ docker pull solr@sha256:53b4d1fe3f65194a35383a6a26ffea6d8b6b16374821481e43bf6532e6cf1905
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
$ docker pull solr@sha256:55e513e1155ffb01d20185f6f20e6ada6b2ac34e9cf215f4721496e4db5a44df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.3 MB (377308729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c941d20a46ce9955f4cfedc5b178a4579a44832396e7588e2faeebdace58bd91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da8ec43a12ff631d1579ab778a0883e59bca58adc86136e1c447ef261a2b6e`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 16.1 MB (16142555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12988e90d6107a2cb56e2156831a2f5e31ac9d7d05cd4abc8fc28b53788d282`  
		Last Modified: Thu, 24 Oct 2024 00:57:17 GMT  
		Size: 46.9 MB (46942141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d133ca2b7f0fb899d954a051126f4c33bfa55975b531ad37c45821e2a63416`  
		Last Modified: Thu, 24 Oct 2024 00:57:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143733ae87a42f42df943534de9fa97f96f238e35ca89d480a4d1acc707d99e0`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147f0c08eb5a1860b96e9f79cda7949c4c8e9df366ee3462f6a25b3260d234af`  
		Last Modified: Thu, 24 Oct 2024 02:00:33 GMT  
		Size: 283.1 MB (283082024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a679f5fa0a7022279ddb1f2fa44361ec87963beed0aa3a73d7b5bb188e006`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 4.3 KB (4272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e6b697443c194d642c9815e9c3abe7cc4033cf613af4f1b0b134ad931ce6f`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95102cf71e5c44c6d11c792fd4cd7ce91ee86c461b29778d00f36463d9a304`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 10.9 KB (10873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a15d322e5a47c927c66983a4f38ad0424650373cd31b9923ff2737538a4db18`  
		Last Modified: Thu, 24 Oct 2024 02:00:28 GMT  
		Size: 1.6 MB (1588494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:9115c4bab259b407e383ef26fbbf28744995939589f79a6407d50ed9183b2ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4331667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042d1555272c7b8872a43b26ff3f7e3db3cf3f1c71d6b4e936bb18295aa070ae`

```dockerfile
```

-	Layers:
	-	`sha256:4a871495ef4f09dd94f49f1a74abc359ba6948c562c9637a3bd9c716ce0369f8`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 4.3 MB (4297621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a91f7e0168fb07ae89d3119209629da10167ee3e638164aa14ca146bfb45833a`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 34.0 KB (34046 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:8980a0c49940f8556f3fadd778dae36b6b3b0688d134456e6154dce1877371af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.4 MB (374398876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5005566bee224901d6e7d791136b804a9dc47c7ab7833ce8b0273adb753cc7a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:cfa18f4f6d476767c7f68ccac923185f893b59c8a9a3b6aca1ee3633822d736d`  
		Last Modified: Thu, 24 Oct 2024 03:52:28 GMT  
		Size: 283.1 MB (283082291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b1523cffe93a957fa5129b22f4a8533a569aea18ed55c257cd64a4a6c134e1`  
		Last Modified: Thu, 24 Oct 2024 03:52:21 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2eba35a90bd0e6200a914d458e9b6e002cbc18161af8d9ca439e24b4fc694d`  
		Last Modified: Thu, 24 Oct 2024 03:52:20 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90829e0839720592600b60d597c1acf14419a4be4c407ffb2706562079d027`  
		Last Modified: Thu, 24 Oct 2024 03:52:20 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc833d5334e15a4601db1bf456deb01976a79ecbfef151f96bbdbefc6a85aacf`  
		Last Modified: Thu, 24 Oct 2024 03:52:22 GMT  
		Size: 1.4 MB (1447415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:801b38c5a8cb95097b32d2631f8e74c80ba19cb911f7fb8b7c94fcb586a49ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594a1541bfe2a946840181c1f80bd58f841b054755bd16ecf68022f60cd5b2a8`

```dockerfile
```

-	Layers:
	-	`sha256:44b3d348eab993108c740128d668d323dedeaea273501e2bd9b23352c127f01e`  
		Last Modified: Thu, 24 Oct 2024 03:52:21 GMT  
		Size: 4.3 MB (4297295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b597425d620193d357a2e5a71a3b1da2458d075448f01978d3e2b4963db5fc`  
		Last Modified: Thu, 24 Oct 2024 03:52:20 GMT  
		Size: 34.2 KB (34212 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9` - linux; ppc64le

```console
$ docker pull solr@sha256:b768517f3165e4bcecd9bf48d9db2e208d42b251ab4a286238ed9d8ec3843bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.6 MB (383555183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087ccfa1f44c73878c90231db1bf12d0eb16fb8cb54c30e5b913926acc0e1043`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ffc205867b9282cd2860676c7adf209ffecaecd41f0da0505d0cdba6237c3`  
		Last Modified: Thu, 24 Oct 2024 01:03:20 GMT  
		Size: 17.6 MB (17648903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bb339e5e3d62195c59a2f131f0e5a6ed308feff23aef3cbbc79ca5cf0d4f20`  
		Last Modified: Thu, 24 Oct 2024 08:59:22 GMT  
		Size: 46.8 MB (46762265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728d0f9756105709617b91992b048ee157aead62b68260a06e5e2e7625eccdc9`  
		Last Modified: Thu, 24 Oct 2024 08:59:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b9035dd65211aa831bbfc2574966166bf420eb3a839a3b8b2859a0ee5eb501`  
		Last Modified: Thu, 24 Oct 2024 08:59:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b784cac8e7184dbb332579e261badf9fae064ab023a40f7a0df38969dba0633`  
		Last Modified: Thu, 24 Oct 2024 12:50:48 GMT  
		Size: 283.1 MB (283082499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d05c055e4c0544aefcb6060039f7838ff53662c6823468799fba7d7f2c0d8f6`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 4.3 KB (4278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677047bbb992ee3ab74888b0980ea2530076530ace578fa76c805f8fd555b0b5`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06293e84babbccd0868e03a001da9a71d5cc8e69f78161e19c52799169ca1450`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 10.9 KB (10876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040124bf55e91141a4b381d95b8a3c9c31259e4798e95cc192b893bc1fec331d`  
		Last Modified: Thu, 24 Oct 2024 12:50:29 GMT  
		Size: 1.6 MB (1595436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:eed71ce1ba855d2483fad97a269f21b4e7c7a77347d2c7388660df2130b51f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7992a76d8739303842534d66800f3577d0e6b186b76e32dbbf3439fee0969c8a`

```dockerfile
```

-	Layers:
	-	`sha256:1c9694e6e4b6c762b8c7c14377e75d2af4067f3c876102d79a3f0aaddbc83aea`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 4.3 MB (4301528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97caf86a97226966acbf17f793f3ce49914be3d7f2419c24c8bfb16a8a3cac06`  
		Last Modified: Thu, 24 Oct 2024 12:50:27 GMT  
		Size: 34.1 KB (34100 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9` - linux; s390x

```console
$ docker pull solr@sha256:d4bd217ed19e8fbc956b7f3b6d80a39caca61879d3d55d2ac5c9f8ccd1dcb754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.7 MB (372722626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ff38bf9e80643188a44a6a4abd63339d186ef1f6a67f10a18245d554166348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:39ab140716f18d2060f597d25330d5c6ac39a79119d68d9118b4b3a088b5413c`  
		Last Modified: Thu, 24 Oct 2024 19:12:24 GMT  
		Size: 283.1 MB (283082425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350dbc069457017d632a861c41e46c6c6a8c66942620fa0d2f5df18061ae328d`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60fa1f16be3d29329813f4a91637677b451f7904fc7b05c87ce84e912525a3c`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0712d193f199cb181ab50c8067ed58ab63aace9b6b4431579e5cf9fd38baae`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 10.9 KB (10879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91a85ba9d92aa36e3fa085402a1983141d09320861109189723aaa37ece0315`  
		Last Modified: Thu, 24 Oct 2024 19:12:20 GMT  
		Size: 1.5 MB (1535509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:63264bf27b1b280dbbc6e3a55887e41f1b24837c4f0876a73c0468b1d2c8f7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4333268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f002b5c06e89a1e751fe4306cbd9e46bf12f89fe81bf670141aa4286e7e328b2`

```dockerfile
```

-	Layers:
	-	`sha256:22e28952a9a0c4e141776cac01aa2651caabd9ba3b039694e835fe4b5086bb4b`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 4.3 MB (4299220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa97fd354f856145e283a9942840278def50d07970b9d9c113adf6b04dc60482`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 34.0 KB (34048 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9-slim`

```console
$ docker pull solr@sha256:5eb3e2e6791020c6d098514594bc6bd16f2a95a7df0f855801af6f5af98169f5
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
$ docker pull solr@sha256:40964796ab6fe55e910a5fe685e6da7b2e3e0e31a489564bca287d0bda855429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159049612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3de85b76de10083c1bab1f6b5a12171e8a2ef31e7daadfc7eee3effab3f148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da8ec43a12ff631d1579ab778a0883e59bca58adc86136e1c447ef261a2b6e`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 16.1 MB (16142555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12988e90d6107a2cb56e2156831a2f5e31ac9d7d05cd4abc8fc28b53788d282`  
		Last Modified: Thu, 24 Oct 2024 00:57:17 GMT  
		Size: 46.9 MB (46942141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d133ca2b7f0fb899d954a051126f4c33bfa55975b531ad37c45821e2a63416`  
		Last Modified: Thu, 24 Oct 2024 00:57:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143733ae87a42f42df943534de9fa97f96f238e35ca89d480a4d1acc707d99e0`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d7aec591b0e44a4d215460758386a00747b4e3a8ad444257dccb4a9cb59a4e`  
		Last Modified: Thu, 24 Oct 2024 01:58:47 GMT  
		Size: 64.8 MB (64822998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340e06e93475dff78694bc4a3544503a4a7de249220c771ec25b8ea0553c3461`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 4.3 KB (4278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcacdd304dd0c44a89b4293a99ecdd4cbe012a4f1e9f626fb89c985c58b0147e`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13bd3a7a475395203027819ec88c32852d0a57d1127e8da5e35d8b3a25462f`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 10.8 KB (10785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a28a9e26fb744d8b852ca9a44aaaad16d58edcef7b9efa56649a6684a4610d0`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 1.6 MB (1588480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:102bf53e7f5711d23184dfacec67b4a5f33cddd6350687f72d86ebbc77f3a2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3845476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a562938ab279592d4a5b361d65380075f6766088ad172839d1eb82887b02289`

```dockerfile
```

-	Layers:
	-	`sha256:aa31d2c50105ffb9fc12fe1223fc599d209ef88a2d3a91d4a1b2dd81b234e54b`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 3.8 MB (3811365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07d8851be781ff022452481aa0e8409fad79212d37142fbf677ce75ae0568d8`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 34.1 KB (34111 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:4f02c8a8caa13c3e1ed17ecceea47f3c03b68634dc8924a74385cbfe734eccc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156139682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6259ce6b1df2c81ece5994d43d97941f4a32fbdeeb869eb82bec9d300bf4a9cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:9dfb94b9234f5635a4f3f1b7a33531f04eaf2646d44835535bc80e3a68c67806`  
		Last Modified: Thu, 24 Oct 2024 03:53:36 GMT  
		Size: 64.8 MB (64823219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3427cb21b786e706d7fe8291673a8277c767485e3eeba2349341cbd20d2a76b4`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bf71f1c11c7b8a90e9c59e794cb00a15d37167f53a57dbcada7e4af374c24d`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581830794970e2c06074ce7365911e8688579329a1f2c4475d7125377a78f6ce`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 10.8 KB (10784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe02ffc6b5254471e60ac5afddb662b178e2a1a1613d4f4581a134149e02032`  
		Last Modified: Thu, 24 Oct 2024 03:53:35 GMT  
		Size: 1.4 MB (1447375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:bf1cba6cdb61b3a454a97f128037bd15a67b24a7f0e4ffec3a37b87987ee6166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3845314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fe00bf30dacc58e90739394a32e6c5794ea7d2b8044880c8891ac5e8bf184f`

```dockerfile
```

-	Layers:
	-	`sha256:e8d608bc96f44c0f3dd88dcebf7061bcaf77762854d1cbda2b3905cbd5c0d1ef`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 3.8 MB (3811039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98db2f3396d1d8d212bd6da681598cd1e6e8d18a8b3eadfad0aa6f61b13ced69`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 34.3 KB (34275 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:d05f9438568e98f45383c9332c43ef259ad1e1af80cf19ac81d0bd0f09318b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165296148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962c0694000052ba1afdc74b7f972a873f18ff5e2950d2f5a8e2d35ac763b3f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ffc205867b9282cd2860676c7adf209ffecaecd41f0da0505d0cdba6237c3`  
		Last Modified: Thu, 24 Oct 2024 01:03:20 GMT  
		Size: 17.6 MB (17648903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bb339e5e3d62195c59a2f131f0e5a6ed308feff23aef3cbbc79ca5cf0d4f20`  
		Last Modified: Thu, 24 Oct 2024 08:59:22 GMT  
		Size: 46.8 MB (46762265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728d0f9756105709617b91992b048ee157aead62b68260a06e5e2e7625eccdc9`  
		Last Modified: Thu, 24 Oct 2024 08:59:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b9035dd65211aa831bbfc2574966166bf420eb3a839a3b8b2859a0ee5eb501`  
		Last Modified: Thu, 24 Oct 2024 08:59:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12243c9e149fc8e3139c49a46347ed7edf2236ddb7bdafc0ac78f83225a38ad3`  
		Last Modified: Thu, 24 Oct 2024 12:52:33 GMT  
		Size: 64.8 MB (64823561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bea8112889d3e93e5ad231ba3c8211dd429bdc67670c26f99620a293f939bed`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 4.3 KB (4277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5550f9ca2158e2089ad4d2278307dd341376da3b785f4137e8e75a785f8be4ea`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f805fcaf602330852dfd317bd440af85cb54de417ae684f2b292ca0b0a44e8`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 10.8 KB (10785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fca39b45a90e3db1101abe7b348a85a86a431f6e480e452e7bcbd1641abdbb0`  
		Last Modified: Thu, 24 Oct 2024 12:52:32 GMT  
		Size: 1.6 MB (1595427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:4ab513cd00a5a682396f16e94a4dacc2fb55c5a3e27c3fbe9a2a36f587c2e9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46883e67f8d4dbd70a13959e4b49756f304da0f5beda3221474767bd0aba660b`

```dockerfile
```

-	Layers:
	-	`sha256:24f632e19ee7b10aec918606dc4c179080f5d57a16ea6789557a169217b72aef`  
		Last Modified: Thu, 24 Oct 2024 12:52:31 GMT  
		Size: 3.8 MB (3815272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:652973b23c00c0a5705727fe8d212bb5ebaf3d46609acb488eea084ba93c2b82`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 34.2 KB (34163 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; s390x

```console
$ docker pull solr@sha256:7188e548522635ec2f0d0736c7e0341dc409be913483e2e5bd62abb83a438c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154463566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9733dee007838a04bb4bd1be56639f65c2bbdc80dac35843ee610c81411f6b02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:71b07ffe6c16d7db1f035370cba068d2dffef7daec53531593a7903a34442ee1`  
		Last Modified: Thu, 24 Oct 2024 19:15:33 GMT  
		Size: 64.8 MB (64823451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1877b3b4ec6dbd457bdb64e365a2f296332d2648afec9347b851ff6742c5ed4a`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3127522c3cb41ed2c2173880a9af9371bc5c7ef67eb92364f609bcded273405c`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed70d90926a04299f2e61c906d04c48950c52390ef14e0574de590035673d879`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 10.8 KB (10788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546c3c877b794ba60c45c830500f0a87ba0282fd975910cf004d920baa5a3e88`  
		Last Modified: Thu, 24 Oct 2024 19:15:32 GMT  
		Size: 1.5 MB (1535508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1f0769cbac26c19c31dd45dacb772228b4fe5c6b4b5cd47523a17afc1bb2f865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3847074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42baf7ec4ed64969c22c8576bd704a54911f086c5f25358f762f26feaca1816`

```dockerfile
```

-	Layers:
	-	`sha256:06a080a59ed7fa83e0d01abeb7bf4cac12da6696d1e42e092137b3a4d60c4924`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 3.8 MB (3812964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7822a0aad6a9041feb4a7c3c535ee3608ddda314ff02eabd456144018c52025e`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.7`

```console
$ docker pull solr@sha256:53b4d1fe3f65194a35383a6a26ffea6d8b6b16374821481e43bf6532e6cf1905
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

### `solr:9.7` - linux; amd64

```console
$ docker pull solr@sha256:55e513e1155ffb01d20185f6f20e6ada6b2ac34e9cf215f4721496e4db5a44df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.3 MB (377308729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c941d20a46ce9955f4cfedc5b178a4579a44832396e7588e2faeebdace58bd91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da8ec43a12ff631d1579ab778a0883e59bca58adc86136e1c447ef261a2b6e`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 16.1 MB (16142555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12988e90d6107a2cb56e2156831a2f5e31ac9d7d05cd4abc8fc28b53788d282`  
		Last Modified: Thu, 24 Oct 2024 00:57:17 GMT  
		Size: 46.9 MB (46942141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d133ca2b7f0fb899d954a051126f4c33bfa55975b531ad37c45821e2a63416`  
		Last Modified: Thu, 24 Oct 2024 00:57:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143733ae87a42f42df943534de9fa97f96f238e35ca89d480a4d1acc707d99e0`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147f0c08eb5a1860b96e9f79cda7949c4c8e9df366ee3462f6a25b3260d234af`  
		Last Modified: Thu, 24 Oct 2024 02:00:33 GMT  
		Size: 283.1 MB (283082024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a679f5fa0a7022279ddb1f2fa44361ec87963beed0aa3a73d7b5bb188e006`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 4.3 KB (4272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e6b697443c194d642c9815e9c3abe7cc4033cf613af4f1b0b134ad931ce6f`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95102cf71e5c44c6d11c792fd4cd7ce91ee86c461b29778d00f36463d9a304`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 10.9 KB (10873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a15d322e5a47c927c66983a4f38ad0424650373cd31b9923ff2737538a4db18`  
		Last Modified: Thu, 24 Oct 2024 02:00:28 GMT  
		Size: 1.6 MB (1588494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7` - unknown; unknown

```console
$ docker pull solr@sha256:9115c4bab259b407e383ef26fbbf28744995939589f79a6407d50ed9183b2ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4331667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042d1555272c7b8872a43b26ff3f7e3db3cf3f1c71d6b4e936bb18295aa070ae`

```dockerfile
```

-	Layers:
	-	`sha256:4a871495ef4f09dd94f49f1a74abc359ba6948c562c9637a3bd9c716ce0369f8`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 4.3 MB (4297621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a91f7e0168fb07ae89d3119209629da10167ee3e638164aa14ca146bfb45833a`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 34.0 KB (34046 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:8980a0c49940f8556f3fadd778dae36b6b3b0688d134456e6154dce1877371af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.4 MB (374398876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5005566bee224901d6e7d791136b804a9dc47c7ab7833ce8b0273adb753cc7a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:cfa18f4f6d476767c7f68ccac923185f893b59c8a9a3b6aca1ee3633822d736d`  
		Last Modified: Thu, 24 Oct 2024 03:52:28 GMT  
		Size: 283.1 MB (283082291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b1523cffe93a957fa5129b22f4a8533a569aea18ed55c257cd64a4a6c134e1`  
		Last Modified: Thu, 24 Oct 2024 03:52:21 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2eba35a90bd0e6200a914d458e9b6e002cbc18161af8d9ca439e24b4fc694d`  
		Last Modified: Thu, 24 Oct 2024 03:52:20 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90829e0839720592600b60d597c1acf14419a4be4c407ffb2706562079d027`  
		Last Modified: Thu, 24 Oct 2024 03:52:20 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc833d5334e15a4601db1bf456deb01976a79ecbfef151f96bbdbefc6a85aacf`  
		Last Modified: Thu, 24 Oct 2024 03:52:22 GMT  
		Size: 1.4 MB (1447415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7` - unknown; unknown

```console
$ docker pull solr@sha256:801b38c5a8cb95097b32d2631f8e74c80ba19cb911f7fb8b7c94fcb586a49ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594a1541bfe2a946840181c1f80bd58f841b054755bd16ecf68022f60cd5b2a8`

```dockerfile
```

-	Layers:
	-	`sha256:44b3d348eab993108c740128d668d323dedeaea273501e2bd9b23352c127f01e`  
		Last Modified: Thu, 24 Oct 2024 03:52:21 GMT  
		Size: 4.3 MB (4297295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b597425d620193d357a2e5a71a3b1da2458d075448f01978d3e2b4963db5fc`  
		Last Modified: Thu, 24 Oct 2024 03:52:20 GMT  
		Size: 34.2 KB (34212 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7` - linux; ppc64le

```console
$ docker pull solr@sha256:b768517f3165e4bcecd9bf48d9db2e208d42b251ab4a286238ed9d8ec3843bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.6 MB (383555183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087ccfa1f44c73878c90231db1bf12d0eb16fb8cb54c30e5b913926acc0e1043`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ffc205867b9282cd2860676c7adf209ffecaecd41f0da0505d0cdba6237c3`  
		Last Modified: Thu, 24 Oct 2024 01:03:20 GMT  
		Size: 17.6 MB (17648903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bb339e5e3d62195c59a2f131f0e5a6ed308feff23aef3cbbc79ca5cf0d4f20`  
		Last Modified: Thu, 24 Oct 2024 08:59:22 GMT  
		Size: 46.8 MB (46762265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728d0f9756105709617b91992b048ee157aead62b68260a06e5e2e7625eccdc9`  
		Last Modified: Thu, 24 Oct 2024 08:59:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b9035dd65211aa831bbfc2574966166bf420eb3a839a3b8b2859a0ee5eb501`  
		Last Modified: Thu, 24 Oct 2024 08:59:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b784cac8e7184dbb332579e261badf9fae064ab023a40f7a0df38969dba0633`  
		Last Modified: Thu, 24 Oct 2024 12:50:48 GMT  
		Size: 283.1 MB (283082499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d05c055e4c0544aefcb6060039f7838ff53662c6823468799fba7d7f2c0d8f6`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 4.3 KB (4278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677047bbb992ee3ab74888b0980ea2530076530ace578fa76c805f8fd555b0b5`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06293e84babbccd0868e03a001da9a71d5cc8e69f78161e19c52799169ca1450`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 10.9 KB (10876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040124bf55e91141a4b381d95b8a3c9c31259e4798e95cc192b893bc1fec331d`  
		Last Modified: Thu, 24 Oct 2024 12:50:29 GMT  
		Size: 1.6 MB (1595436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7` - unknown; unknown

```console
$ docker pull solr@sha256:eed71ce1ba855d2483fad97a269f21b4e7c7a77347d2c7388660df2130b51f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7992a76d8739303842534d66800f3577d0e6b186b76e32dbbf3439fee0969c8a`

```dockerfile
```

-	Layers:
	-	`sha256:1c9694e6e4b6c762b8c7c14377e75d2af4067f3c876102d79a3f0aaddbc83aea`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 4.3 MB (4301528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97caf86a97226966acbf17f793f3ce49914be3d7f2419c24c8bfb16a8a3cac06`  
		Last Modified: Thu, 24 Oct 2024 12:50:27 GMT  
		Size: 34.1 KB (34100 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7` - linux; s390x

```console
$ docker pull solr@sha256:d4bd217ed19e8fbc956b7f3b6d80a39caca61879d3d55d2ac5c9f8ccd1dcb754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.7 MB (372722626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ff38bf9e80643188a44a6a4abd63339d186ef1f6a67f10a18245d554166348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:39ab140716f18d2060f597d25330d5c6ac39a79119d68d9118b4b3a088b5413c`  
		Last Modified: Thu, 24 Oct 2024 19:12:24 GMT  
		Size: 283.1 MB (283082425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350dbc069457017d632a861c41e46c6c6a8c66942620fa0d2f5df18061ae328d`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60fa1f16be3d29329813f4a91637677b451f7904fc7b05c87ce84e912525a3c`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0712d193f199cb181ab50c8067ed58ab63aace9b6b4431579e5cf9fd38baae`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 10.9 KB (10879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91a85ba9d92aa36e3fa085402a1983141d09320861109189723aaa37ece0315`  
		Last Modified: Thu, 24 Oct 2024 19:12:20 GMT  
		Size: 1.5 MB (1535509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7` - unknown; unknown

```console
$ docker pull solr@sha256:63264bf27b1b280dbbc6e3a55887e41f1b24837c4f0876a73c0468b1d2c8f7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4333268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f002b5c06e89a1e751fe4306cbd9e46bf12f89fe81bf670141aa4286e7e328b2`

```dockerfile
```

-	Layers:
	-	`sha256:22e28952a9a0c4e141776cac01aa2651caabd9ba3b039694e835fe4b5086bb4b`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 4.3 MB (4299220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa97fd354f856145e283a9942840278def50d07970b9d9c113adf6b04dc60482`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 34.0 KB (34048 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.7-slim`

```console
$ docker pull solr@sha256:5eb3e2e6791020c6d098514594bc6bd16f2a95a7df0f855801af6f5af98169f5
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

### `solr:9.7-slim` - linux; amd64

```console
$ docker pull solr@sha256:40964796ab6fe55e910a5fe685e6da7b2e3e0e31a489564bca287d0bda855429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159049612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3de85b76de10083c1bab1f6b5a12171e8a2ef31e7daadfc7eee3effab3f148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da8ec43a12ff631d1579ab778a0883e59bca58adc86136e1c447ef261a2b6e`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 16.1 MB (16142555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12988e90d6107a2cb56e2156831a2f5e31ac9d7d05cd4abc8fc28b53788d282`  
		Last Modified: Thu, 24 Oct 2024 00:57:17 GMT  
		Size: 46.9 MB (46942141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d133ca2b7f0fb899d954a051126f4c33bfa55975b531ad37c45821e2a63416`  
		Last Modified: Thu, 24 Oct 2024 00:57:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143733ae87a42f42df943534de9fa97f96f238e35ca89d480a4d1acc707d99e0`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d7aec591b0e44a4d215460758386a00747b4e3a8ad444257dccb4a9cb59a4e`  
		Last Modified: Thu, 24 Oct 2024 01:58:47 GMT  
		Size: 64.8 MB (64822998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340e06e93475dff78694bc4a3544503a4a7de249220c771ec25b8ea0553c3461`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 4.3 KB (4278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcacdd304dd0c44a89b4293a99ecdd4cbe012a4f1e9f626fb89c985c58b0147e`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13bd3a7a475395203027819ec88c32852d0a57d1127e8da5e35d8b3a25462f`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 10.8 KB (10785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a28a9e26fb744d8b852ca9a44aaaad16d58edcef7b9efa56649a6684a4610d0`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 1.6 MB (1588480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7-slim` - unknown; unknown

```console
$ docker pull solr@sha256:102bf53e7f5711d23184dfacec67b4a5f33cddd6350687f72d86ebbc77f3a2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3845476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a562938ab279592d4a5b361d65380075f6766088ad172839d1eb82887b02289`

```dockerfile
```

-	Layers:
	-	`sha256:aa31d2c50105ffb9fc12fe1223fc599d209ef88a2d3a91d4a1b2dd81b234e54b`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 3.8 MB (3811365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07d8851be781ff022452481aa0e8409fad79212d37142fbf677ce75ae0568d8`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 34.1 KB (34111 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:4f02c8a8caa13c3e1ed17ecceea47f3c03b68634dc8924a74385cbfe734eccc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156139682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6259ce6b1df2c81ece5994d43d97941f4a32fbdeeb869eb82bec9d300bf4a9cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:9dfb94b9234f5635a4f3f1b7a33531f04eaf2646d44835535bc80e3a68c67806`  
		Last Modified: Thu, 24 Oct 2024 03:53:36 GMT  
		Size: 64.8 MB (64823219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3427cb21b786e706d7fe8291673a8277c767485e3eeba2349341cbd20d2a76b4`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bf71f1c11c7b8a90e9c59e794cb00a15d37167f53a57dbcada7e4af374c24d`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581830794970e2c06074ce7365911e8688579329a1f2c4475d7125377a78f6ce`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 10.8 KB (10784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe02ffc6b5254471e60ac5afddb662b178e2a1a1613d4f4581a134149e02032`  
		Last Modified: Thu, 24 Oct 2024 03:53:35 GMT  
		Size: 1.4 MB (1447375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7-slim` - unknown; unknown

```console
$ docker pull solr@sha256:bf1cba6cdb61b3a454a97f128037bd15a67b24a7f0e4ffec3a37b87987ee6166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3845314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fe00bf30dacc58e90739394a32e6c5794ea7d2b8044880c8891ac5e8bf184f`

```dockerfile
```

-	Layers:
	-	`sha256:e8d608bc96f44c0f3dd88dcebf7061bcaf77762854d1cbda2b3905cbd5c0d1ef`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 3.8 MB (3811039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98db2f3396d1d8d212bd6da681598cd1e6e8d18a8b3eadfad0aa6f61b13ced69`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 34.3 KB (34275 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:d05f9438568e98f45383c9332c43ef259ad1e1af80cf19ac81d0bd0f09318b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165296148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962c0694000052ba1afdc74b7f972a873f18ff5e2950d2f5a8e2d35ac763b3f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ffc205867b9282cd2860676c7adf209ffecaecd41f0da0505d0cdba6237c3`  
		Last Modified: Thu, 24 Oct 2024 01:03:20 GMT  
		Size: 17.6 MB (17648903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bb339e5e3d62195c59a2f131f0e5a6ed308feff23aef3cbbc79ca5cf0d4f20`  
		Last Modified: Thu, 24 Oct 2024 08:59:22 GMT  
		Size: 46.8 MB (46762265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728d0f9756105709617b91992b048ee157aead62b68260a06e5e2e7625eccdc9`  
		Last Modified: Thu, 24 Oct 2024 08:59:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b9035dd65211aa831bbfc2574966166bf420eb3a839a3b8b2859a0ee5eb501`  
		Last Modified: Thu, 24 Oct 2024 08:59:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12243c9e149fc8e3139c49a46347ed7edf2236ddb7bdafc0ac78f83225a38ad3`  
		Last Modified: Thu, 24 Oct 2024 12:52:33 GMT  
		Size: 64.8 MB (64823561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bea8112889d3e93e5ad231ba3c8211dd429bdc67670c26f99620a293f939bed`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 4.3 KB (4277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5550f9ca2158e2089ad4d2278307dd341376da3b785f4137e8e75a785f8be4ea`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f805fcaf602330852dfd317bd440af85cb54de417ae684f2b292ca0b0a44e8`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 10.8 KB (10785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fca39b45a90e3db1101abe7b348a85a86a431f6e480e452e7bcbd1641abdbb0`  
		Last Modified: Thu, 24 Oct 2024 12:52:32 GMT  
		Size: 1.6 MB (1595427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7-slim` - unknown; unknown

```console
$ docker pull solr@sha256:4ab513cd00a5a682396f16e94a4dacc2fb55c5a3e27c3fbe9a2a36f587c2e9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46883e67f8d4dbd70a13959e4b49756f304da0f5beda3221474767bd0aba660b`

```dockerfile
```

-	Layers:
	-	`sha256:24f632e19ee7b10aec918606dc4c179080f5d57a16ea6789557a169217b72aef`  
		Last Modified: Thu, 24 Oct 2024 12:52:31 GMT  
		Size: 3.8 MB (3815272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:652973b23c00c0a5705727fe8d212bb5ebaf3d46609acb488eea084ba93c2b82`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 34.2 KB (34163 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7-slim` - linux; s390x

```console
$ docker pull solr@sha256:7188e548522635ec2f0d0736c7e0341dc409be913483e2e5bd62abb83a438c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154463566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9733dee007838a04bb4bd1be56639f65c2bbdc80dac35843ee610c81411f6b02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:71b07ffe6c16d7db1f035370cba068d2dffef7daec53531593a7903a34442ee1`  
		Last Modified: Thu, 24 Oct 2024 19:15:33 GMT  
		Size: 64.8 MB (64823451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1877b3b4ec6dbd457bdb64e365a2f296332d2648afec9347b851ff6742c5ed4a`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3127522c3cb41ed2c2173880a9af9371bc5c7ef67eb92364f609bcded273405c`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed70d90926a04299f2e61c906d04c48950c52390ef14e0574de590035673d879`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 10.8 KB (10788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546c3c877b794ba60c45c830500f0a87ba0282fd975910cf004d920baa5a3e88`  
		Last Modified: Thu, 24 Oct 2024 19:15:32 GMT  
		Size: 1.5 MB (1535508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1f0769cbac26c19c31dd45dacb772228b4fe5c6b4b5cd47523a17afc1bb2f865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3847074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42baf7ec4ed64969c22c8576bd704a54911f086c5f25358f762f26feaca1816`

```dockerfile
```

-	Layers:
	-	`sha256:06a080a59ed7fa83e0d01abeb7bf4cac12da6696d1e42e092137b3a4d60c4924`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 3.8 MB (3812964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7822a0aad6a9041feb4a7c3c535ee3608ddda314ff02eabd456144018c52025e`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.7.0`

```console
$ docker pull solr@sha256:53b4d1fe3f65194a35383a6a26ffea6d8b6b16374821481e43bf6532e6cf1905
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

### `solr:9.7.0` - linux; amd64

```console
$ docker pull solr@sha256:55e513e1155ffb01d20185f6f20e6ada6b2ac34e9cf215f4721496e4db5a44df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.3 MB (377308729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c941d20a46ce9955f4cfedc5b178a4579a44832396e7588e2faeebdace58bd91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da8ec43a12ff631d1579ab778a0883e59bca58adc86136e1c447ef261a2b6e`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 16.1 MB (16142555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12988e90d6107a2cb56e2156831a2f5e31ac9d7d05cd4abc8fc28b53788d282`  
		Last Modified: Thu, 24 Oct 2024 00:57:17 GMT  
		Size: 46.9 MB (46942141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d133ca2b7f0fb899d954a051126f4c33bfa55975b531ad37c45821e2a63416`  
		Last Modified: Thu, 24 Oct 2024 00:57:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143733ae87a42f42df943534de9fa97f96f238e35ca89d480a4d1acc707d99e0`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147f0c08eb5a1860b96e9f79cda7949c4c8e9df366ee3462f6a25b3260d234af`  
		Last Modified: Thu, 24 Oct 2024 02:00:33 GMT  
		Size: 283.1 MB (283082024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a679f5fa0a7022279ddb1f2fa44361ec87963beed0aa3a73d7b5bb188e006`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 4.3 KB (4272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e6b697443c194d642c9815e9c3abe7cc4033cf613af4f1b0b134ad931ce6f`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95102cf71e5c44c6d11c792fd4cd7ce91ee86c461b29778d00f36463d9a304`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 10.9 KB (10873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a15d322e5a47c927c66983a4f38ad0424650373cd31b9923ff2737538a4db18`  
		Last Modified: Thu, 24 Oct 2024 02:00:28 GMT  
		Size: 1.6 MB (1588494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0` - unknown; unknown

```console
$ docker pull solr@sha256:9115c4bab259b407e383ef26fbbf28744995939589f79a6407d50ed9183b2ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4331667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042d1555272c7b8872a43b26ff3f7e3db3cf3f1c71d6b4e936bb18295aa070ae`

```dockerfile
```

-	Layers:
	-	`sha256:4a871495ef4f09dd94f49f1a74abc359ba6948c562c9637a3bd9c716ce0369f8`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 4.3 MB (4297621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a91f7e0168fb07ae89d3119209629da10167ee3e638164aa14ca146bfb45833a`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 34.0 KB (34046 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7.0` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:8980a0c49940f8556f3fadd778dae36b6b3b0688d134456e6154dce1877371af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.4 MB (374398876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5005566bee224901d6e7d791136b804a9dc47c7ab7833ce8b0273adb753cc7a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:cfa18f4f6d476767c7f68ccac923185f893b59c8a9a3b6aca1ee3633822d736d`  
		Last Modified: Thu, 24 Oct 2024 03:52:28 GMT  
		Size: 283.1 MB (283082291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b1523cffe93a957fa5129b22f4a8533a569aea18ed55c257cd64a4a6c134e1`  
		Last Modified: Thu, 24 Oct 2024 03:52:21 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2eba35a90bd0e6200a914d458e9b6e002cbc18161af8d9ca439e24b4fc694d`  
		Last Modified: Thu, 24 Oct 2024 03:52:20 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90829e0839720592600b60d597c1acf14419a4be4c407ffb2706562079d027`  
		Last Modified: Thu, 24 Oct 2024 03:52:20 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc833d5334e15a4601db1bf456deb01976a79ecbfef151f96bbdbefc6a85aacf`  
		Last Modified: Thu, 24 Oct 2024 03:52:22 GMT  
		Size: 1.4 MB (1447415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0` - unknown; unknown

```console
$ docker pull solr@sha256:801b38c5a8cb95097b32d2631f8e74c80ba19cb911f7fb8b7c94fcb586a49ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594a1541bfe2a946840181c1f80bd58f841b054755bd16ecf68022f60cd5b2a8`

```dockerfile
```

-	Layers:
	-	`sha256:44b3d348eab993108c740128d668d323dedeaea273501e2bd9b23352c127f01e`  
		Last Modified: Thu, 24 Oct 2024 03:52:21 GMT  
		Size: 4.3 MB (4297295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b597425d620193d357a2e5a71a3b1da2458d075448f01978d3e2b4963db5fc`  
		Last Modified: Thu, 24 Oct 2024 03:52:20 GMT  
		Size: 34.2 KB (34212 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7.0` - linux; ppc64le

```console
$ docker pull solr@sha256:b768517f3165e4bcecd9bf48d9db2e208d42b251ab4a286238ed9d8ec3843bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.6 MB (383555183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087ccfa1f44c73878c90231db1bf12d0eb16fb8cb54c30e5b913926acc0e1043`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ffc205867b9282cd2860676c7adf209ffecaecd41f0da0505d0cdba6237c3`  
		Last Modified: Thu, 24 Oct 2024 01:03:20 GMT  
		Size: 17.6 MB (17648903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bb339e5e3d62195c59a2f131f0e5a6ed308feff23aef3cbbc79ca5cf0d4f20`  
		Last Modified: Thu, 24 Oct 2024 08:59:22 GMT  
		Size: 46.8 MB (46762265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728d0f9756105709617b91992b048ee157aead62b68260a06e5e2e7625eccdc9`  
		Last Modified: Thu, 24 Oct 2024 08:59:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b9035dd65211aa831bbfc2574966166bf420eb3a839a3b8b2859a0ee5eb501`  
		Last Modified: Thu, 24 Oct 2024 08:59:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b784cac8e7184dbb332579e261badf9fae064ab023a40f7a0df38969dba0633`  
		Last Modified: Thu, 24 Oct 2024 12:50:48 GMT  
		Size: 283.1 MB (283082499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d05c055e4c0544aefcb6060039f7838ff53662c6823468799fba7d7f2c0d8f6`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 4.3 KB (4278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677047bbb992ee3ab74888b0980ea2530076530ace578fa76c805f8fd555b0b5`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06293e84babbccd0868e03a001da9a71d5cc8e69f78161e19c52799169ca1450`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 10.9 KB (10876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040124bf55e91141a4b381d95b8a3c9c31259e4798e95cc192b893bc1fec331d`  
		Last Modified: Thu, 24 Oct 2024 12:50:29 GMT  
		Size: 1.6 MB (1595436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0` - unknown; unknown

```console
$ docker pull solr@sha256:eed71ce1ba855d2483fad97a269f21b4e7c7a77347d2c7388660df2130b51f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7992a76d8739303842534d66800f3577d0e6b186b76e32dbbf3439fee0969c8a`

```dockerfile
```

-	Layers:
	-	`sha256:1c9694e6e4b6c762b8c7c14377e75d2af4067f3c876102d79a3f0aaddbc83aea`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 4.3 MB (4301528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97caf86a97226966acbf17f793f3ce49914be3d7f2419c24c8bfb16a8a3cac06`  
		Last Modified: Thu, 24 Oct 2024 12:50:27 GMT  
		Size: 34.1 KB (34100 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7.0` - linux; s390x

```console
$ docker pull solr@sha256:d4bd217ed19e8fbc956b7f3b6d80a39caca61879d3d55d2ac5c9f8ccd1dcb754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.7 MB (372722626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ff38bf9e80643188a44a6a4abd63339d186ef1f6a67f10a18245d554166348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:39ab140716f18d2060f597d25330d5c6ac39a79119d68d9118b4b3a088b5413c`  
		Last Modified: Thu, 24 Oct 2024 19:12:24 GMT  
		Size: 283.1 MB (283082425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350dbc069457017d632a861c41e46c6c6a8c66942620fa0d2f5df18061ae328d`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60fa1f16be3d29329813f4a91637677b451f7904fc7b05c87ce84e912525a3c`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0712d193f199cb181ab50c8067ed58ab63aace9b6b4431579e5cf9fd38baae`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 10.9 KB (10879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91a85ba9d92aa36e3fa085402a1983141d09320861109189723aaa37ece0315`  
		Last Modified: Thu, 24 Oct 2024 19:12:20 GMT  
		Size: 1.5 MB (1535509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0` - unknown; unknown

```console
$ docker pull solr@sha256:63264bf27b1b280dbbc6e3a55887e41f1b24837c4f0876a73c0468b1d2c8f7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4333268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f002b5c06e89a1e751fe4306cbd9e46bf12f89fe81bf670141aa4286e7e328b2`

```dockerfile
```

-	Layers:
	-	`sha256:22e28952a9a0c4e141776cac01aa2651caabd9ba3b039694e835fe4b5086bb4b`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 4.3 MB (4299220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa97fd354f856145e283a9942840278def50d07970b9d9c113adf6b04dc60482`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 34.0 KB (34048 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.7.0-slim`

```console
$ docker pull solr@sha256:5eb3e2e6791020c6d098514594bc6bd16f2a95a7df0f855801af6f5af98169f5
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

### `solr:9.7.0-slim` - linux; amd64

```console
$ docker pull solr@sha256:40964796ab6fe55e910a5fe685e6da7b2e3e0e31a489564bca287d0bda855429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159049612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3de85b76de10083c1bab1f6b5a12171e8a2ef31e7daadfc7eee3effab3f148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da8ec43a12ff631d1579ab778a0883e59bca58adc86136e1c447ef261a2b6e`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 16.1 MB (16142555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12988e90d6107a2cb56e2156831a2f5e31ac9d7d05cd4abc8fc28b53788d282`  
		Last Modified: Thu, 24 Oct 2024 00:57:17 GMT  
		Size: 46.9 MB (46942141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d133ca2b7f0fb899d954a051126f4c33bfa55975b531ad37c45821e2a63416`  
		Last Modified: Thu, 24 Oct 2024 00:57:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143733ae87a42f42df943534de9fa97f96f238e35ca89d480a4d1acc707d99e0`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d7aec591b0e44a4d215460758386a00747b4e3a8ad444257dccb4a9cb59a4e`  
		Last Modified: Thu, 24 Oct 2024 01:58:47 GMT  
		Size: 64.8 MB (64822998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340e06e93475dff78694bc4a3544503a4a7de249220c771ec25b8ea0553c3461`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 4.3 KB (4278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcacdd304dd0c44a89b4293a99ecdd4cbe012a4f1e9f626fb89c985c58b0147e`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13bd3a7a475395203027819ec88c32852d0a57d1127e8da5e35d8b3a25462f`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 10.8 KB (10785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a28a9e26fb744d8b852ca9a44aaaad16d58edcef7b9efa56649a6684a4610d0`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 1.6 MB (1588480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:102bf53e7f5711d23184dfacec67b4a5f33cddd6350687f72d86ebbc77f3a2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3845476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a562938ab279592d4a5b361d65380075f6766088ad172839d1eb82887b02289`

```dockerfile
```

-	Layers:
	-	`sha256:aa31d2c50105ffb9fc12fe1223fc599d209ef88a2d3a91d4a1b2dd81b234e54b`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 3.8 MB (3811365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07d8851be781ff022452481aa0e8409fad79212d37142fbf677ce75ae0568d8`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 34.1 KB (34111 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7.0-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:4f02c8a8caa13c3e1ed17ecceea47f3c03b68634dc8924a74385cbfe734eccc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156139682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6259ce6b1df2c81ece5994d43d97941f4a32fbdeeb869eb82bec9d300bf4a9cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:9dfb94b9234f5635a4f3f1b7a33531f04eaf2646d44835535bc80e3a68c67806`  
		Last Modified: Thu, 24 Oct 2024 03:53:36 GMT  
		Size: 64.8 MB (64823219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3427cb21b786e706d7fe8291673a8277c767485e3eeba2349341cbd20d2a76b4`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bf71f1c11c7b8a90e9c59e794cb00a15d37167f53a57dbcada7e4af374c24d`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581830794970e2c06074ce7365911e8688579329a1f2c4475d7125377a78f6ce`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 10.8 KB (10784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe02ffc6b5254471e60ac5afddb662b178e2a1a1613d4f4581a134149e02032`  
		Last Modified: Thu, 24 Oct 2024 03:53:35 GMT  
		Size: 1.4 MB (1447375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:bf1cba6cdb61b3a454a97f128037bd15a67b24a7f0e4ffec3a37b87987ee6166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3845314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fe00bf30dacc58e90739394a32e6c5794ea7d2b8044880c8891ac5e8bf184f`

```dockerfile
```

-	Layers:
	-	`sha256:e8d608bc96f44c0f3dd88dcebf7061bcaf77762854d1cbda2b3905cbd5c0d1ef`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 3.8 MB (3811039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98db2f3396d1d8d212bd6da681598cd1e6e8d18a8b3eadfad0aa6f61b13ced69`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 34.3 KB (34275 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7.0-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:d05f9438568e98f45383c9332c43ef259ad1e1af80cf19ac81d0bd0f09318b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165296148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962c0694000052ba1afdc74b7f972a873f18ff5e2950d2f5a8e2d35ac763b3f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ffc205867b9282cd2860676c7adf209ffecaecd41f0da0505d0cdba6237c3`  
		Last Modified: Thu, 24 Oct 2024 01:03:20 GMT  
		Size: 17.6 MB (17648903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bb339e5e3d62195c59a2f131f0e5a6ed308feff23aef3cbbc79ca5cf0d4f20`  
		Last Modified: Thu, 24 Oct 2024 08:59:22 GMT  
		Size: 46.8 MB (46762265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728d0f9756105709617b91992b048ee157aead62b68260a06e5e2e7625eccdc9`  
		Last Modified: Thu, 24 Oct 2024 08:59:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b9035dd65211aa831bbfc2574966166bf420eb3a839a3b8b2859a0ee5eb501`  
		Last Modified: Thu, 24 Oct 2024 08:59:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12243c9e149fc8e3139c49a46347ed7edf2236ddb7bdafc0ac78f83225a38ad3`  
		Last Modified: Thu, 24 Oct 2024 12:52:33 GMT  
		Size: 64.8 MB (64823561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bea8112889d3e93e5ad231ba3c8211dd429bdc67670c26f99620a293f939bed`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 4.3 KB (4277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5550f9ca2158e2089ad4d2278307dd341376da3b785f4137e8e75a785f8be4ea`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f805fcaf602330852dfd317bd440af85cb54de417ae684f2b292ca0b0a44e8`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 10.8 KB (10785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fca39b45a90e3db1101abe7b348a85a86a431f6e480e452e7bcbd1641abdbb0`  
		Last Modified: Thu, 24 Oct 2024 12:52:32 GMT  
		Size: 1.6 MB (1595427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:4ab513cd00a5a682396f16e94a4dacc2fb55c5a3e27c3fbe9a2a36f587c2e9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46883e67f8d4dbd70a13959e4b49756f304da0f5beda3221474767bd0aba660b`

```dockerfile
```

-	Layers:
	-	`sha256:24f632e19ee7b10aec918606dc4c179080f5d57a16ea6789557a169217b72aef`  
		Last Modified: Thu, 24 Oct 2024 12:52:31 GMT  
		Size: 3.8 MB (3815272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:652973b23c00c0a5705727fe8d212bb5ebaf3d46609acb488eea084ba93c2b82`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 34.2 KB (34163 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7.0-slim` - linux; s390x

```console
$ docker pull solr@sha256:7188e548522635ec2f0d0736c7e0341dc409be913483e2e5bd62abb83a438c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154463566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9733dee007838a04bb4bd1be56639f65c2bbdc80dac35843ee610c81411f6b02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:71b07ffe6c16d7db1f035370cba068d2dffef7daec53531593a7903a34442ee1`  
		Last Modified: Thu, 24 Oct 2024 19:15:33 GMT  
		Size: 64.8 MB (64823451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1877b3b4ec6dbd457bdb64e365a2f296332d2648afec9347b851ff6742c5ed4a`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3127522c3cb41ed2c2173880a9af9371bc5c7ef67eb92364f609bcded273405c`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed70d90926a04299f2e61c906d04c48950c52390ef14e0574de590035673d879`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 10.8 KB (10788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546c3c877b794ba60c45c830500f0a87ba0282fd975910cf004d920baa5a3e88`  
		Last Modified: Thu, 24 Oct 2024 19:15:32 GMT  
		Size: 1.5 MB (1535508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1f0769cbac26c19c31dd45dacb772228b4fe5c6b4b5cd47523a17afc1bb2f865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3847074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42baf7ec4ed64969c22c8576bd704a54911f086c5f25358f762f26feaca1816`

```dockerfile
```

-	Layers:
	-	`sha256:06a080a59ed7fa83e0d01abeb7bf4cac12da6696d1e42e092137b3a4d60c4924`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 3.8 MB (3812964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7822a0aad6a9041feb4a7c3c535ee3608ddda314ff02eabd456144018c52025e`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.8`

```console
$ docker pull solr@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `solr:9.8-slim`

```console
$ docker pull solr@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `solr:9.8.0`

```console
$ docker pull solr@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `solr:9.8.0-slim`

```console
$ docker pull solr@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `solr:latest`

```console
$ docker pull solr@sha256:53b4d1fe3f65194a35383a6a26ffea6d8b6b16374821481e43bf6532e6cf1905
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
$ docker pull solr@sha256:55e513e1155ffb01d20185f6f20e6ada6b2ac34e9cf215f4721496e4db5a44df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.3 MB (377308729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c941d20a46ce9955f4cfedc5b178a4579a44832396e7588e2faeebdace58bd91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da8ec43a12ff631d1579ab778a0883e59bca58adc86136e1c447ef261a2b6e`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 16.1 MB (16142555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12988e90d6107a2cb56e2156831a2f5e31ac9d7d05cd4abc8fc28b53788d282`  
		Last Modified: Thu, 24 Oct 2024 00:57:17 GMT  
		Size: 46.9 MB (46942141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d133ca2b7f0fb899d954a051126f4c33bfa55975b531ad37c45821e2a63416`  
		Last Modified: Thu, 24 Oct 2024 00:57:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143733ae87a42f42df943534de9fa97f96f238e35ca89d480a4d1acc707d99e0`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147f0c08eb5a1860b96e9f79cda7949c4c8e9df366ee3462f6a25b3260d234af`  
		Last Modified: Thu, 24 Oct 2024 02:00:33 GMT  
		Size: 283.1 MB (283082024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20a679f5fa0a7022279ddb1f2fa44361ec87963beed0aa3a73d7b5bb188e006`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 4.3 KB (4272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e6b697443c194d642c9815e9c3abe7cc4033cf613af4f1b0b134ad931ce6f`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95102cf71e5c44c6d11c792fd4cd7ce91ee86c461b29778d00f36463d9a304`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 10.9 KB (10873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a15d322e5a47c927c66983a4f38ad0424650373cd31b9923ff2737538a4db18`  
		Last Modified: Thu, 24 Oct 2024 02:00:28 GMT  
		Size: 1.6 MB (1588494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:9115c4bab259b407e383ef26fbbf28744995939589f79a6407d50ed9183b2ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4331667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042d1555272c7b8872a43b26ff3f7e3db3cf3f1c71d6b4e936bb18295aa070ae`

```dockerfile
```

-	Layers:
	-	`sha256:4a871495ef4f09dd94f49f1a74abc359ba6948c562c9637a3bd9c716ce0369f8`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 4.3 MB (4297621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a91f7e0168fb07ae89d3119209629da10167ee3e638164aa14ca146bfb45833a`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 34.0 KB (34046 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:8980a0c49940f8556f3fadd778dae36b6b3b0688d134456e6154dce1877371af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.4 MB (374398876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5005566bee224901d6e7d791136b804a9dc47c7ab7833ce8b0273adb753cc7a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:cfa18f4f6d476767c7f68ccac923185f893b59c8a9a3b6aca1ee3633822d736d`  
		Last Modified: Thu, 24 Oct 2024 03:52:28 GMT  
		Size: 283.1 MB (283082291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b1523cffe93a957fa5129b22f4a8533a569aea18ed55c257cd64a4a6c134e1`  
		Last Modified: Thu, 24 Oct 2024 03:52:21 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2eba35a90bd0e6200a914d458e9b6e002cbc18161af8d9ca439e24b4fc694d`  
		Last Modified: Thu, 24 Oct 2024 03:52:20 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90829e0839720592600b60d597c1acf14419a4be4c407ffb2706562079d027`  
		Last Modified: Thu, 24 Oct 2024 03:52:20 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc833d5334e15a4601db1bf456deb01976a79ecbfef151f96bbdbefc6a85aacf`  
		Last Modified: Thu, 24 Oct 2024 03:52:22 GMT  
		Size: 1.4 MB (1447415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:801b38c5a8cb95097b32d2631f8e74c80ba19cb911f7fb8b7c94fcb586a49ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594a1541bfe2a946840181c1f80bd58f841b054755bd16ecf68022f60cd5b2a8`

```dockerfile
```

-	Layers:
	-	`sha256:44b3d348eab993108c740128d668d323dedeaea273501e2bd9b23352c127f01e`  
		Last Modified: Thu, 24 Oct 2024 03:52:21 GMT  
		Size: 4.3 MB (4297295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b597425d620193d357a2e5a71a3b1da2458d075448f01978d3e2b4963db5fc`  
		Last Modified: Thu, 24 Oct 2024 03:52:20 GMT  
		Size: 34.2 KB (34212 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:b768517f3165e4bcecd9bf48d9db2e208d42b251ab4a286238ed9d8ec3843bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.6 MB (383555183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087ccfa1f44c73878c90231db1bf12d0eb16fb8cb54c30e5b913926acc0e1043`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ffc205867b9282cd2860676c7adf209ffecaecd41f0da0505d0cdba6237c3`  
		Last Modified: Thu, 24 Oct 2024 01:03:20 GMT  
		Size: 17.6 MB (17648903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bb339e5e3d62195c59a2f131f0e5a6ed308feff23aef3cbbc79ca5cf0d4f20`  
		Last Modified: Thu, 24 Oct 2024 08:59:22 GMT  
		Size: 46.8 MB (46762265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728d0f9756105709617b91992b048ee157aead62b68260a06e5e2e7625eccdc9`  
		Last Modified: Thu, 24 Oct 2024 08:59:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b9035dd65211aa831bbfc2574966166bf420eb3a839a3b8b2859a0ee5eb501`  
		Last Modified: Thu, 24 Oct 2024 08:59:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b784cac8e7184dbb332579e261badf9fae064ab023a40f7a0df38969dba0633`  
		Last Modified: Thu, 24 Oct 2024 12:50:48 GMT  
		Size: 283.1 MB (283082499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d05c055e4c0544aefcb6060039f7838ff53662c6823468799fba7d7f2c0d8f6`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 4.3 KB (4278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677047bbb992ee3ab74888b0980ea2530076530ace578fa76c805f8fd555b0b5`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06293e84babbccd0868e03a001da9a71d5cc8e69f78161e19c52799169ca1450`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 10.9 KB (10876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040124bf55e91141a4b381d95b8a3c9c31259e4798e95cc192b893bc1fec331d`  
		Last Modified: Thu, 24 Oct 2024 12:50:29 GMT  
		Size: 1.6 MB (1595436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:eed71ce1ba855d2483fad97a269f21b4e7c7a77347d2c7388660df2130b51f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7992a76d8739303842534d66800f3577d0e6b186b76e32dbbf3439fee0969c8a`

```dockerfile
```

-	Layers:
	-	`sha256:1c9694e6e4b6c762b8c7c14377e75d2af4067f3c876102d79a3f0aaddbc83aea`  
		Last Modified: Thu, 24 Oct 2024 12:50:28 GMT  
		Size: 4.3 MB (4301528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97caf86a97226966acbf17f793f3ce49914be3d7f2419c24c8bfb16a8a3cac06`  
		Last Modified: Thu, 24 Oct 2024 12:50:27 GMT  
		Size: 34.1 KB (34100 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:d4bd217ed19e8fbc956b7f3b6d80a39caca61879d3d55d2ac5c9f8ccd1dcb754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.7 MB (372722626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ff38bf9e80643188a44a6a4abd63339d186ef1f6a67f10a18245d554166348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST= SOLR_SHA512=a80417a79c8371d2049868573927c587b4a5b7b37e938ca6e64e8a8842449f49eddc987968ddad5d6b6b1f4395990c1edc4576a884b3a62c4fbcd97091a659d9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:39ab140716f18d2060f597d25330d5c6ac39a79119d68d9118b4b3a088b5413c`  
		Last Modified: Thu, 24 Oct 2024 19:12:24 GMT  
		Size: 283.1 MB (283082425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350dbc069457017d632a861c41e46c6c6a8c66942620fa0d2f5df18061ae328d`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60fa1f16be3d29329813f4a91637677b451f7904fc7b05c87ce84e912525a3c`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0712d193f199cb181ab50c8067ed58ab63aace9b6b4431579e5cf9fd38baae`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 10.9 KB (10879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91a85ba9d92aa36e3fa085402a1983141d09320861109189723aaa37ece0315`  
		Last Modified: Thu, 24 Oct 2024 19:12:20 GMT  
		Size: 1.5 MB (1535509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:63264bf27b1b280dbbc6e3a55887e41f1b24837c4f0876a73c0468b1d2c8f7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4333268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f002b5c06e89a1e751fe4306cbd9e46bf12f89fe81bf670141aa4286e7e328b2`

```dockerfile
```

-	Layers:
	-	`sha256:22e28952a9a0c4e141776cac01aa2651caabd9ba3b039694e835fe4b5086bb4b`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 4.3 MB (4299220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa97fd354f856145e283a9942840278def50d07970b9d9c113adf6b04dc60482`  
		Last Modified: Thu, 24 Oct 2024 19:12:18 GMT  
		Size: 34.0 KB (34048 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:slim`

```console
$ docker pull solr@sha256:5eb3e2e6791020c6d098514594bc6bd16f2a95a7df0f855801af6f5af98169f5
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
$ docker pull solr@sha256:40964796ab6fe55e910a5fe685e6da7b2e3e0e31a489564bca287d0bda855429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159049612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3de85b76de10083c1bab1f6b5a12171e8a2ef31e7daadfc7eee3effab3f148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da8ec43a12ff631d1579ab778a0883e59bca58adc86136e1c447ef261a2b6e`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 16.1 MB (16142555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12988e90d6107a2cb56e2156831a2f5e31ac9d7d05cd4abc8fc28b53788d282`  
		Last Modified: Thu, 24 Oct 2024 00:57:17 GMT  
		Size: 46.9 MB (46942141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d133ca2b7f0fb899d954a051126f4c33bfa55975b531ad37c45821e2a63416`  
		Last Modified: Thu, 24 Oct 2024 00:57:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143733ae87a42f42df943534de9fa97f96f238e35ca89d480a4d1acc707d99e0`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d7aec591b0e44a4d215460758386a00747b4e3a8ad444257dccb4a9cb59a4e`  
		Last Modified: Thu, 24 Oct 2024 01:58:47 GMT  
		Size: 64.8 MB (64822998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340e06e93475dff78694bc4a3544503a4a7de249220c771ec25b8ea0553c3461`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 4.3 KB (4278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcacdd304dd0c44a89b4293a99ecdd4cbe012a4f1e9f626fb89c985c58b0147e`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d13bd3a7a475395203027819ec88c32852d0a57d1127e8da5e35d8b3a25462f`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 10.8 KB (10785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a28a9e26fb744d8b852ca9a44aaaad16d58edcef7b9efa56649a6684a4610d0`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 1.6 MB (1588480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:102bf53e7f5711d23184dfacec67b4a5f33cddd6350687f72d86ebbc77f3a2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3845476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a562938ab279592d4a5b361d65380075f6766088ad172839d1eb82887b02289`

```dockerfile
```

-	Layers:
	-	`sha256:aa31d2c50105ffb9fc12fe1223fc599d209ef88a2d3a91d4a1b2dd81b234e54b`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 3.8 MB (3811365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07d8851be781ff022452481aa0e8409fad79212d37142fbf677ce75ae0568d8`  
		Last Modified: Thu, 24 Oct 2024 01:58:46 GMT  
		Size: 34.1 KB (34111 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:4f02c8a8caa13c3e1ed17ecceea47f3c03b68634dc8924a74385cbfe734eccc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156139682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6259ce6b1df2c81ece5994d43d97941f4a32fbdeeb869eb82bec9d300bf4a9cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:9dfb94b9234f5635a4f3f1b7a33531f04eaf2646d44835535bc80e3a68c67806`  
		Last Modified: Thu, 24 Oct 2024 03:53:36 GMT  
		Size: 64.8 MB (64823219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3427cb21b786e706d7fe8291673a8277c767485e3eeba2349341cbd20d2a76b4`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bf71f1c11c7b8a90e9c59e794cb00a15d37167f53a57dbcada7e4af374c24d`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581830794970e2c06074ce7365911e8688579329a1f2c4475d7125377a78f6ce`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 10.8 KB (10784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe02ffc6b5254471e60ac5afddb662b178e2a1a1613d4f4581a134149e02032`  
		Last Modified: Thu, 24 Oct 2024 03:53:35 GMT  
		Size: 1.4 MB (1447375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:bf1cba6cdb61b3a454a97f128037bd15a67b24a7f0e4ffec3a37b87987ee6166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3845314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fe00bf30dacc58e90739394a32e6c5794ea7d2b8044880c8891ac5e8bf184f`

```dockerfile
```

-	Layers:
	-	`sha256:e8d608bc96f44c0f3dd88dcebf7061bcaf77762854d1cbda2b3905cbd5c0d1ef`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 3.8 MB (3811039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98db2f3396d1d8d212bd6da681598cd1e6e8d18a8b3eadfad0aa6f61b13ced69`  
		Last Modified: Thu, 24 Oct 2024 03:53:34 GMT  
		Size: 34.3 KB (34275 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; ppc64le

```console
$ docker pull solr@sha256:d05f9438568e98f45383c9332c43ef259ad1e1af80cf19ac81d0bd0f09318b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165296148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962c0694000052ba1afdc74b7f972a873f18ff5e2950d2f5a8e2d35ac763b3f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17ffc205867b9282cd2860676c7adf209ffecaecd41f0da0505d0cdba6237c3`  
		Last Modified: Thu, 24 Oct 2024 01:03:20 GMT  
		Size: 17.6 MB (17648903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bb339e5e3d62195c59a2f131f0e5a6ed308feff23aef3cbbc79ca5cf0d4f20`  
		Last Modified: Thu, 24 Oct 2024 08:59:22 GMT  
		Size: 46.8 MB (46762265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728d0f9756105709617b91992b048ee157aead62b68260a06e5e2e7625eccdc9`  
		Last Modified: Thu, 24 Oct 2024 08:59:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b9035dd65211aa831bbfc2574966166bf420eb3a839a3b8b2859a0ee5eb501`  
		Last Modified: Thu, 24 Oct 2024 08:59:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12243c9e149fc8e3139c49a46347ed7edf2236ddb7bdafc0ac78f83225a38ad3`  
		Last Modified: Thu, 24 Oct 2024 12:52:33 GMT  
		Size: 64.8 MB (64823561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bea8112889d3e93e5ad231ba3c8211dd429bdc67670c26f99620a293f939bed`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 4.3 KB (4277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5550f9ca2158e2089ad4d2278307dd341376da3b785f4137e8e75a785f8be4ea`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f805fcaf602330852dfd317bd440af85cb54de417ae684f2b292ca0b0a44e8`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 10.8 KB (10785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fca39b45a90e3db1101abe7b348a85a86a431f6e480e452e7bcbd1641abdbb0`  
		Last Modified: Thu, 24 Oct 2024 12:52:32 GMT  
		Size: 1.6 MB (1595427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:4ab513cd00a5a682396f16e94a4dacc2fb55c5a3e27c3fbe9a2a36f587c2e9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46883e67f8d4dbd70a13959e4b49756f304da0f5beda3221474767bd0aba660b`

```dockerfile
```

-	Layers:
	-	`sha256:24f632e19ee7b10aec918606dc4c179080f5d57a16ea6789557a169217b72aef`  
		Last Modified: Thu, 24 Oct 2024 12:52:31 GMT  
		Size: 3.8 MB (3815272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:652973b23c00c0a5705727fe8d212bb5ebaf3d46609acb488eea084ba93c2b82`  
		Last Modified: Thu, 24 Oct 2024 12:52:30 GMT  
		Size: 34.2 KB (34163 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; s390x

```console
$ docker pull solr@sha256:7188e548522635ec2f0d0736c7e0341dc409be913483e2e5bd62abb83a438c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154463566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9733dee007838a04bb4bd1be56639f65c2bbdc80dac35843ee610c81411f6b02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 09 Sep 2024 16:43:56 GMT
ARG RELEASE
# Mon, 09 Sep 2024 16:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 16:43:56 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Mon, 09 Sep 2024 16:43:56 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Sep 2024 16:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 16:43:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_VERSION=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DIST=-slim
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Mon, 09 Sep 2024 16:43:56 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.version=9.7.0
# Mon, 09 Sep 2024 16:43:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Mon, 09 Sep 2024 16:43:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
# ARGS: SOLR_VERSION=9.7.0 SOLR_DIST=-slim SOLR_SHA512=f270ebd94deb9a002fb4e57c5cc2c11c7acc583dfa8e65a814028aa22dd8d0fa7c8a18f92024d8c0f5b07853801d25dcb2e26b3b3d4c8b2d906485f8dc0224c9 SOLR_KEYS=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 09 Sep 2024 16:43:56 GMT
VOLUME [/var/solr]
# Mon, 09 Sep 2024 16:43:56 GMT
EXPOSE map[8983/tcp:{}]
# Mon, 09 Sep 2024 16:43:56 GMT
WORKDIR /opt/solr
# Mon, 09 Sep 2024 16:43:56 GMT
USER 8983
# Mon, 09 Sep 2024 16:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Sep 2024 16:43:56 GMT
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
	-	`sha256:71b07ffe6c16d7db1f035370cba068d2dffef7daec53531593a7903a34442ee1`  
		Last Modified: Thu, 24 Oct 2024 19:15:33 GMT  
		Size: 64.8 MB (64823451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1877b3b4ec6dbd457bdb64e365a2f296332d2648afec9347b851ff6742c5ed4a`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3127522c3cb41ed2c2173880a9af9371bc5c7ef67eb92364f609bcded273405c`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed70d90926a04299f2e61c906d04c48950c52390ef14e0574de590035673d879`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 10.8 KB (10788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546c3c877b794ba60c45c830500f0a87ba0282fd975910cf004d920baa5a3e88`  
		Last Modified: Thu, 24 Oct 2024 19:15:32 GMT  
		Size: 1.5 MB (1535508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:1f0769cbac26c19c31dd45dacb772228b4fe5c6b4b5cd47523a17afc1bb2f865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3847074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42baf7ec4ed64969c22c8576bd704a54911f086c5f25358f762f26feaca1816`

```dockerfile
```

-	Layers:
	-	`sha256:06a080a59ed7fa83e0d01abeb7bf4cac12da6696d1e42e092137b3a4d60c4924`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 3.8 MB (3812964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7822a0aad6a9041feb4a7c3c535ee3608ddda314ff02eabd456144018c52025e`  
		Last Modified: Thu, 24 Oct 2024 19:15:31 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json
