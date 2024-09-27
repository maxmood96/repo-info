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
-	[`solr:9.6`](#solr96)
-	[`solr:9.6-slim`](#solr96-slim)
-	[`solr:9.6.1`](#solr961)
-	[`solr:9.6.1-slim`](#solr961-slim)
-	[`solr:9.7`](#solr97)
-	[`solr:9.7-slim`](#solr97-slim)
-	[`solr:9.7.0`](#solr970)
-	[`solr:9.7.0-slim`](#solr970-slim)
-	[`solr:latest`](#solrlatest)
-	[`solr:slim`](#solrslim)

## `solr:8`

```console
$ docker pull solr@sha256:6a63293030eb1110fd81b1c6f5edc4711ba719a3d6d4b93211d1f179af96f180
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
$ docker pull solr@sha256:c5d27cb1a075801217cc7463bbca9725943a2186bc61062cc999f010bdcc4d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.1 MB (323134323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:defb8f5bfd3bbf979184e306d510eac3baef5e8a6d72d0e67741e76aaebe565b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46bdbd88e5c97485003310b142bf5c3c58bb9677087aed67152e8d6e4d5f47a`  
		Last Modified: Fri, 23 Aug 2024 19:26:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7efbf9e7d7c55fd4a7d7cf86817e5dc3128427e806a1576d8ddb50d04f937`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 5.0 MB (5002678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0454dc334683a867cfdf81593cd7b353df482767a2efeb2223d43c19c3fe9ed`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a486d837e8bce146166479fe29d4f1d4cd0a87fa3c5ae95ed711432f1a95fbff`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 2.9 KB (2887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5c31765272d843b81a4a150390c4f9e150f075e04eca5d675ab639be77f7ea`  
		Last Modified: Thu, 26 Sep 2024 22:57:19 GMT  
		Size: 225.4 MB (225414053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edff86e4fdd655e5933db69bd0dd6268deceb49d51b11ca70e200fe7fc2cac4`  
		Last Modified: Thu, 26 Sep 2024 22:57:17 GMT  
		Size: 6.3 KB (6271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8` - unknown; unknown

```console
$ docker pull solr@sha256:84507e96b4ccd30467dba7b3effe3dadf152d4c2043b728f481708d459907eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37de412a80c202573995c9e9279c78eed6abb7ac93deb38a7993b33b0b2af5f6`

```dockerfile
```

-	Layers:
	-	`sha256:12880be67fb3782d6d958b78721173d27e737948a2a63f920dbc1947ac53178f`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 4.1 MB (4138633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef11850f7f236d2edb6deaadc40dae95ba4cd13ade40a89e03c07c3692725eb5`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 36.3 KB (36306 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:a041f470477aaa4c3793a97a1d815d864492dc39e9e76856c477b3f59f498bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319543360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfab67d60d3c38eacee040aea03205bf495cbf9ad840f70a001fdea86ebebbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Feb 2024 17:48:20 GMT
ARG RELEASE
# Fri, 09 Feb 2024 17:48:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 09 Feb 2024 17:48:20 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 09 Feb 2024 17:48:20 GMT
CMD ["/bin/bash"]
# Fri, 09 Feb 2024 17:48:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Feb 2024 17:48:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 17:48:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_VERSION=8.11.3
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512 # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=https://www.apache.org/dyn/closer.lua/lucene/solr/8.11.3/solr-8.11.3.tgz?action=download SOLR_DIST_URL=https://downloads.apache.org/lucene/solr/8.11.3/solr-8.11.3.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.3/solr-8.11.3.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0 # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME" # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
COPY --chown=0:0 scripts /opt/docker-solr/scripts # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
VOLUME [/var/solr]
# Fri, 09 Feb 2024 17:48:20 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 09 Feb 2024 17:48:20 GMT
WORKDIR /opt/solr
# Fri, 09 Feb 2024 17:48:20 GMT
USER 8983
# Fri, 09 Feb 2024 17:48:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Feb 2024 17:48:20 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5a032d75137abf4a646016d6785211957158b7f98ae6bb407f805900f78fc3`  
		Last Modified: Fri, 23 Aug 2024 19:44:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3bd09a8851024db763b997267026cea779ccfb044a389f4b33b4523b80f2da`  
		Last Modified: Sat, 24 Aug 2024 01:17:03 GMT  
		Size: 4.8 MB (4847845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03dc8d97e607d7fac177424ea1a33965f09a1b390b3d9e5783819b8a9b5c77a`  
		Last Modified: Sat, 24 Aug 2024 01:17:02 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fb5486658b2efd5ff1f1a764a3f8e2b30c4e03df4aabb32f4f5d81d67ab759`  
		Last Modified: Sat, 24 Aug 2024 01:17:02 GMT  
		Size: 2.9 KB (2887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1515c20df83019401b79bca95fecac43a6459e851b42a0ae70827e8b8018a50`  
		Last Modified: Sat, 24 Aug 2024 01:17:08 GMT  
		Size: 225.1 MB (225140286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ef938ef4a607f3c3561a75b5191d336ffdc63517ff3d70336a5c816baf160`  
		Last Modified: Sat, 24 Aug 2024 01:17:03 GMT  
		Size: 6.3 KB (6274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8` - unknown; unknown

```console
$ docker pull solr@sha256:218306d33468e1eb26502e51eb815168d6e3ae75a71cc5b9ab3133dc47e5d83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4093998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7409bd4ecb91c2c71df5d988218bef07be48a8030dad02ad04f8929491f0f51b`

```dockerfile
```

-	Layers:
	-	`sha256:6944215fde17e89e1fadcdb7587aec56b3ec666893328c44ca02f45e389b67d6`  
		Last Modified: Sat, 24 Aug 2024 01:17:02 GMT  
		Size: 4.1 MB (4057387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf1e513fad5387dd3106e22abd6b31ce619d8234837fb6d21ec3b52ad6c65cc`  
		Last Modified: Sat, 24 Aug 2024 01:17:02 GMT  
		Size: 36.6 KB (36611 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8` - linux; ppc64le

```console
$ docker pull solr@sha256:772dfc9f12cadcf6f85ff524683a4e7573f54415729da2977ab8e555c5058ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325561187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88f3f07586d3b1345665a65f6f029c290e7006136acb1340c4496ac9aaefd20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef025249b0fe621dd5c39de7e56c0ca2be3a550f30946c0103b22cfb65ce0adf`  
		Last Modified: Wed, 05 Jun 2024 04:00:00 GMT  
		Size: 18.2 MB (18222028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909ebbc0bdbd07a40e729bb5b958f22d12e3d154aded190a6cc48e187be81dda`  
		Last Modified: Wed, 24 Jul 2024 04:13:08 GMT  
		Size: 42.7 MB (42652860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f0c163d60b8d17f187a1ce7c28da5c01c3d9a83bde0f609ee802566ab0e06`  
		Last Modified: Wed, 24 Jul 2024 04:13:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faea3162e16d0b444fcf9c459996557e5d1f601adf99cf73c760b8b9878e23b3`  
		Last Modified: Fri, 23 Aug 2024 19:22:59 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58ded00e5023aa126be34126538a4e90e35049e008185370718a123aea1af66`  
		Last Modified: Fri, 27 Sep 2024 01:13:59 GMT  
		Size: 5.9 MB (5940371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5857d29f36440e77a94b7b991b4b98a02ef6a38e9c24c8bdf4c5ccfa8b267c`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 4.3 KB (4284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da4f0c6ee2bd598c44b83fc37ec27923255e7aa8b50bf44d6c3d6c967638463`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5205c994a40e4d1c8c9b615e657ccdc7c748001d58f14ce918028833d94c359f`  
		Last Modified: Fri, 27 Sep 2024 01:14:07 GMT  
		Size: 225.4 MB (225414061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70f48f8e04453528ada753058672d725ef0147cc0943d9eb67d70f5074c9c39`  
		Last Modified: Fri, 27 Sep 2024 01:13:59 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8` - unknown; unknown

```console
$ docker pull solr@sha256:62bb5f0059253f82691951e26d3a3cf21615154b877358973fd6b22f10eb29bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4178856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ac39df8fac4b59e075e61b8327a644ad232e2bc1e0b7c1152dc82a1422db36`

```dockerfile
```

-	Layers:
	-	`sha256:11b6e886a94f119b611024c9ed5c2ec34ba06e8515d89f224753b305838b64f1`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 4.1 MB (4142513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a84dcf1da08de05c4cc25a5562a96fb48c7724ca86e6107a147ecd923098be`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 36.3 KB (36343 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8` - linux; s390x

```console
$ docker pull solr@sha256:f9c59847a1fe3a79da4b53fa9f8533d45a9eb0158af0b014fc86f49d186f7682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314738218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893395ae57b3f59ef1481b44ab1aa5eee040bf4949770070a8885a3c76bd1407`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a156a04bb486c4a1c69c74a9f01dce29f2e013ccab4e6631197f6cc4d8f4c45`  
		Last Modified: Wed, 05 Jun 2024 03:12:17 GMT  
		Size: 16.6 MB (16645456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd37eed98237b35cbfd9c26e61e50843a3e5cd2ebf664c58e31194178944624f`  
		Last Modified: Wed, 24 Jul 2024 00:57:17 GMT  
		Size: 40.8 MB (40818422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6348169ce0d5dbce34a24949a87f35c57f8e5f9d5b1913297de765327f3c20fd`  
		Last Modified: Wed, 24 Jul 2024 00:57:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946104babcd64d4c66119ed87d279d67861c1c2de97404720c98f6ab72c28479`  
		Last Modified: Fri, 23 Aug 2024 19:47:03 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9660b7bfd361d49c9aaf46a8bc5d0c6cfc12cf3f3a5a2b41d79275a772ad9396`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.8 MB (4831179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de1dc16a9b667a45206e90d3b993c443e1ecca9efcc1d2028cc7c19cbb53fee`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548613fbd3494a92c63c875bd3d8d421fe1b0fc893400c1f6a5c13638f930d3d`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8490c3a9d42d5364f6c44f2655ffc8281d3d341cf8f234614a6f845aa90f3fe`  
		Last Modified: Fri, 27 Sep 2024 00:38:02 GMT  
		Size: 225.4 MB (225413966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9931af8cd7f65fb31294e2278dd8819007cb5b6bc05a561e8b4e737189171b5`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8` - unknown; unknown

```console
$ docker pull solr@sha256:3739dbde80f6c36a899ca27963e4a5e54d8fb428f4c310f563cf5e58487f3dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1d143b13416c0df91eb78ec917a934267d6c94a021c6ef3355120c1f1892d6`

```dockerfile
```

-	Layers:
	-	`sha256:7d7205f14935b77276edb09bf5a4f2c0837e9318b83c00cefb02f588cccda61c`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.1 MB (4139433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:456e7de9073c15fd7ed08d73abf6627293e03677d3743c178f57e5693a7f72f2`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 36.3 KB (36306 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:8-slim`

```console
$ docker pull solr@sha256:ce41841bc3268ca1b5dd4b67c4b9b18fffce35efdadda479efb78336b76f684a
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
$ docker pull solr@sha256:01c980db779d0405cca055e90f9b565072ef7a64a6a2bef41362019f80408872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.1 MB (323134341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be727de2c22da89cbc0833683bc2f307b4c56bf3e6033a8aca82c49c07de5d12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46bdbd88e5c97485003310b142bf5c3c58bb9677087aed67152e8d6e4d5f47a`  
		Last Modified: Fri, 23 Aug 2024 19:26:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3044a2a9f396b20a6931ca7450fc5f5cf720d6e3fbe0b429cc04587dfb4fbb6a`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 5.0 MB (5002685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d83292bf77153932bf1eaeebd0ceb3031180626dd45af424f532c7ef69ba9f8`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 4.3 KB (4277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d73245baa2d25922e06245c53de062e9ec67c2623518fe4e5afd6e2b8fa60d`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a45605e444e6e20345a76c0b9216f3101d8d1e2421c5883d653960fc35e0e5`  
		Last Modified: Thu, 26 Sep 2024 22:57:19 GMT  
		Size: 225.4 MB (225414058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4ad173f326ed826d2c3d6a42998533c8f43f146e735ccb6410e0510cc8ed1d`  
		Last Modified: Thu, 26 Sep 2024 22:57:17 GMT  
		Size: 6.3 KB (6273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:b593d3aa0fd4fc5cba37d26cc5e47df34fe50ad2ff817d7e88397cb4bfe8606f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5f0061d678ecf66773b11a7bcdf5a3e785949db3f7000bc8600a7a0fb26d1d`

```dockerfile
```

-	Layers:
	-	`sha256:a809e5f60af1efff54ce1503161ddde484632f76893b6e03df9ca60539b29df1`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 4.1 MB (4138663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:139d637f919e7b9c2b548536fa87100379bc7c431771406cd8f4ee14a8fb9847`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 36.4 KB (36355 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:f49929f952f41d07353fce812472fff89521e8a08d9a165122e4d5627eff9e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319543360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfab67d60d3c38eacee040aea03205bf495cbf9ad840f70a001fdea86ebebbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Feb 2024 17:48:20 GMT
ARG RELEASE
# Fri, 09 Feb 2024 17:48:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 09 Feb 2024 17:48:20 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 09 Feb 2024 17:48:20 GMT
CMD ["/bin/bash"]
# Fri, 09 Feb 2024 17:48:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Feb 2024 17:48:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 17:48:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_VERSION=8.11.3
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512 # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=https://www.apache.org/dyn/closer.lua/lucene/solr/8.11.3/solr-8.11.3.tgz?action=download SOLR_DIST_URL=https://downloads.apache.org/lucene/solr/8.11.3/solr-8.11.3.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.3/solr-8.11.3.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0 # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME" # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
COPY --chown=0:0 scripts /opt/docker-solr/scripts # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
VOLUME [/var/solr]
# Fri, 09 Feb 2024 17:48:20 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 09 Feb 2024 17:48:20 GMT
WORKDIR /opt/solr
# Fri, 09 Feb 2024 17:48:20 GMT
USER 8983
# Fri, 09 Feb 2024 17:48:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Feb 2024 17:48:20 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5a032d75137abf4a646016d6785211957158b7f98ae6bb407f805900f78fc3`  
		Last Modified: Fri, 23 Aug 2024 19:44:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3bd09a8851024db763b997267026cea779ccfb044a389f4b33b4523b80f2da`  
		Last Modified: Sat, 24 Aug 2024 01:17:03 GMT  
		Size: 4.8 MB (4847845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03dc8d97e607d7fac177424ea1a33965f09a1b390b3d9e5783819b8a9b5c77a`  
		Last Modified: Sat, 24 Aug 2024 01:17:02 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fb5486658b2efd5ff1f1a764a3f8e2b30c4e03df4aabb32f4f5d81d67ab759`  
		Last Modified: Sat, 24 Aug 2024 01:17:02 GMT  
		Size: 2.9 KB (2887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1515c20df83019401b79bca95fecac43a6459e851b42a0ae70827e8b8018a50`  
		Last Modified: Sat, 24 Aug 2024 01:17:08 GMT  
		Size: 225.1 MB (225140286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ef938ef4a607f3c3561a75b5191d336ffdc63517ff3d70336a5c816baf160`  
		Last Modified: Sat, 24 Aug 2024 01:17:03 GMT  
		Size: 6.3 KB (6274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:a1ea3e659687e9f8c2b5c7582be7051ef9483172f338eb358ddcfdc7c1223b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4094077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710f0e1aa69f9485eedae4357d82aaf5cc1e1b2a2b315e60626434f853deca7b`

```dockerfile
```

-	Layers:
	-	`sha256:3eaaeb2d1e01fb91bf382d513b72118aa0800dea42a8352457b486b1799eccec`  
		Last Modified: Sat, 24 Aug 2024 01:17:36 GMT  
		Size: 4.1 MB (4057417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e106e70638bc59f5dd76b0ad2d3ecb928934479a70764f7946f0c3b9d5c7f06`  
		Last Modified: Sat, 24 Aug 2024 01:17:36 GMT  
		Size: 36.7 KB (36660 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:4a058c28c45983da0e54185a752c5f50cb72afb1cc063ad306a3e7a952814cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325561187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88f3f07586d3b1345665a65f6f029c290e7006136acb1340c4496ac9aaefd20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef025249b0fe621dd5c39de7e56c0ca2be3a550f30946c0103b22cfb65ce0adf`  
		Last Modified: Wed, 05 Jun 2024 04:00:00 GMT  
		Size: 18.2 MB (18222028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909ebbc0bdbd07a40e729bb5b958f22d12e3d154aded190a6cc48e187be81dda`  
		Last Modified: Wed, 24 Jul 2024 04:13:08 GMT  
		Size: 42.7 MB (42652860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f0c163d60b8d17f187a1ce7c28da5c01c3d9a83bde0f609ee802566ab0e06`  
		Last Modified: Wed, 24 Jul 2024 04:13:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faea3162e16d0b444fcf9c459996557e5d1f601adf99cf73c760b8b9878e23b3`  
		Last Modified: Fri, 23 Aug 2024 19:22:59 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58ded00e5023aa126be34126538a4e90e35049e008185370718a123aea1af66`  
		Last Modified: Fri, 27 Sep 2024 01:13:59 GMT  
		Size: 5.9 MB (5940371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5857d29f36440e77a94b7b991b4b98a02ef6a38e9c24c8bdf4c5ccfa8b267c`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 4.3 KB (4284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da4f0c6ee2bd598c44b83fc37ec27923255e7aa8b50bf44d6c3d6c967638463`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5205c994a40e4d1c8c9b615e657ccdc7c748001d58f14ce918028833d94c359f`  
		Last Modified: Fri, 27 Sep 2024 01:14:07 GMT  
		Size: 225.4 MB (225414061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70f48f8e04453528ada753058672d725ef0147cc0943d9eb67d70f5074c9c39`  
		Last Modified: Fri, 27 Sep 2024 01:13:59 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:ff8f1ee348694d97e824badb92b4b34480e3368725edae8d1d906a6ea600c653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4178936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcb2a16ef989a3435c7db236ab60442092b0c89303b3ffcb18203c64b77f528`

```dockerfile
```

-	Layers:
	-	`sha256:c5dcbd5ecdaa07abcc20069025e065bab53521264cc5edfd56094fbd6273316d`  
		Last Modified: Fri, 27 Sep 2024 01:14:55 GMT  
		Size: 4.1 MB (4142543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d17b39e08c4502d5db7d1a69143163b1bd21d32e35baa28294ba619c7cd3ed7`  
		Last Modified: Fri, 27 Sep 2024 01:14:54 GMT  
		Size: 36.4 KB (36393 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; s390x

```console
$ docker pull solr@sha256:e3fdde108d6bc2c4f8625650c8fe0a426248232a32ac0e5bb387598d1c27ec97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314738218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893395ae57b3f59ef1481b44ab1aa5eee040bf4949770070a8885a3c76bd1407`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a156a04bb486c4a1c69c74a9f01dce29f2e013ccab4e6631197f6cc4d8f4c45`  
		Last Modified: Wed, 05 Jun 2024 03:12:17 GMT  
		Size: 16.6 MB (16645456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd37eed98237b35cbfd9c26e61e50843a3e5cd2ebf664c58e31194178944624f`  
		Last Modified: Wed, 24 Jul 2024 00:57:17 GMT  
		Size: 40.8 MB (40818422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6348169ce0d5dbce34a24949a87f35c57f8e5f9d5b1913297de765327f3c20fd`  
		Last Modified: Wed, 24 Jul 2024 00:57:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946104babcd64d4c66119ed87d279d67861c1c2de97404720c98f6ab72c28479`  
		Last Modified: Fri, 23 Aug 2024 19:47:03 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9660b7bfd361d49c9aaf46a8bc5d0c6cfc12cf3f3a5a2b41d79275a772ad9396`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.8 MB (4831179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de1dc16a9b667a45206e90d3b993c443e1ecca9efcc1d2028cc7c19cbb53fee`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548613fbd3494a92c63c875bd3d8d421fe1b0fc893400c1f6a5c13638f930d3d`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8490c3a9d42d5364f6c44f2655ffc8281d3d341cf8f234614a6f845aa90f3fe`  
		Last Modified: Fri, 27 Sep 2024 00:38:02 GMT  
		Size: 225.4 MB (225413966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9931af8cd7f65fb31294e2278dd8819007cb5b6bc05a561e8b4e737189171b5`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:bfe99b6c2a89bae7413e4cab75a5d1929a5e92ea052dfee84157732d24f8d2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b9697ba081a8fc94b54777b7e167a98651e24aa8b1340e6bca057bef5c01a1`

```dockerfile
```

-	Layers:
	-	`sha256:066325287907bb4fa898d3b1a6e296e8c961f2e78bff52008c1b869c41572a39`  
		Last Modified: Fri, 27 Sep 2024 00:38:47 GMT  
		Size: 4.1 MB (4139463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60e102343a5d9563aef8ea32fdc4299b94b4a3086b2c9f3ca08587be8add80a1`  
		Last Modified: Fri, 27 Sep 2024 00:38:47 GMT  
		Size: 36.4 KB (36355 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:8.11`

```console
$ docker pull solr@sha256:6a63293030eb1110fd81b1c6f5edc4711ba719a3d6d4b93211d1f179af96f180
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
$ docker pull solr@sha256:c5d27cb1a075801217cc7463bbca9725943a2186bc61062cc999f010bdcc4d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.1 MB (323134323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:defb8f5bfd3bbf979184e306d510eac3baef5e8a6d72d0e67741e76aaebe565b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46bdbd88e5c97485003310b142bf5c3c58bb9677087aed67152e8d6e4d5f47a`  
		Last Modified: Fri, 23 Aug 2024 19:26:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7efbf9e7d7c55fd4a7d7cf86817e5dc3128427e806a1576d8ddb50d04f937`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 5.0 MB (5002678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0454dc334683a867cfdf81593cd7b353df482767a2efeb2223d43c19c3fe9ed`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a486d837e8bce146166479fe29d4f1d4cd0a87fa3c5ae95ed711432f1a95fbff`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 2.9 KB (2887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5c31765272d843b81a4a150390c4f9e150f075e04eca5d675ab639be77f7ea`  
		Last Modified: Thu, 26 Sep 2024 22:57:19 GMT  
		Size: 225.4 MB (225414053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edff86e4fdd655e5933db69bd0dd6268deceb49d51b11ca70e200fe7fc2cac4`  
		Last Modified: Thu, 26 Sep 2024 22:57:17 GMT  
		Size: 6.3 KB (6271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11` - unknown; unknown

```console
$ docker pull solr@sha256:84507e96b4ccd30467dba7b3effe3dadf152d4c2043b728f481708d459907eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37de412a80c202573995c9e9279c78eed6abb7ac93deb38a7993b33b0b2af5f6`

```dockerfile
```

-	Layers:
	-	`sha256:12880be67fb3782d6d958b78721173d27e737948a2a63f920dbc1947ac53178f`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 4.1 MB (4138633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef11850f7f236d2edb6deaadc40dae95ba4cd13ade40a89e03c07c3692725eb5`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 36.3 KB (36306 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:a041f470477aaa4c3793a97a1d815d864492dc39e9e76856c477b3f59f498bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319543360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfab67d60d3c38eacee040aea03205bf495cbf9ad840f70a001fdea86ebebbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Feb 2024 17:48:20 GMT
ARG RELEASE
# Fri, 09 Feb 2024 17:48:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 09 Feb 2024 17:48:20 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 09 Feb 2024 17:48:20 GMT
CMD ["/bin/bash"]
# Fri, 09 Feb 2024 17:48:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Feb 2024 17:48:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 17:48:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_VERSION=8.11.3
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512 # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=https://www.apache.org/dyn/closer.lua/lucene/solr/8.11.3/solr-8.11.3.tgz?action=download SOLR_DIST_URL=https://downloads.apache.org/lucene/solr/8.11.3/solr-8.11.3.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.3/solr-8.11.3.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0 # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME" # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
COPY --chown=0:0 scripts /opt/docker-solr/scripts # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
VOLUME [/var/solr]
# Fri, 09 Feb 2024 17:48:20 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 09 Feb 2024 17:48:20 GMT
WORKDIR /opt/solr
# Fri, 09 Feb 2024 17:48:20 GMT
USER 8983
# Fri, 09 Feb 2024 17:48:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Feb 2024 17:48:20 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5a032d75137abf4a646016d6785211957158b7f98ae6bb407f805900f78fc3`  
		Last Modified: Fri, 23 Aug 2024 19:44:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3bd09a8851024db763b997267026cea779ccfb044a389f4b33b4523b80f2da`  
		Last Modified: Sat, 24 Aug 2024 01:17:03 GMT  
		Size: 4.8 MB (4847845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03dc8d97e607d7fac177424ea1a33965f09a1b390b3d9e5783819b8a9b5c77a`  
		Last Modified: Sat, 24 Aug 2024 01:17:02 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fb5486658b2efd5ff1f1a764a3f8e2b30c4e03df4aabb32f4f5d81d67ab759`  
		Last Modified: Sat, 24 Aug 2024 01:17:02 GMT  
		Size: 2.9 KB (2887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1515c20df83019401b79bca95fecac43a6459e851b42a0ae70827e8b8018a50`  
		Last Modified: Sat, 24 Aug 2024 01:17:08 GMT  
		Size: 225.1 MB (225140286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ef938ef4a607f3c3561a75b5191d336ffdc63517ff3d70336a5c816baf160`  
		Last Modified: Sat, 24 Aug 2024 01:17:03 GMT  
		Size: 6.3 KB (6274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11` - unknown; unknown

```console
$ docker pull solr@sha256:218306d33468e1eb26502e51eb815168d6e3ae75a71cc5b9ab3133dc47e5d83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4093998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7409bd4ecb91c2c71df5d988218bef07be48a8030dad02ad04f8929491f0f51b`

```dockerfile
```

-	Layers:
	-	`sha256:6944215fde17e89e1fadcdb7587aec56b3ec666893328c44ca02f45e389b67d6`  
		Last Modified: Sat, 24 Aug 2024 01:17:02 GMT  
		Size: 4.1 MB (4057387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf1e513fad5387dd3106e22abd6b31ce619d8234837fb6d21ec3b52ad6c65cc`  
		Last Modified: Sat, 24 Aug 2024 01:17:02 GMT  
		Size: 36.6 KB (36611 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11` - linux; ppc64le

```console
$ docker pull solr@sha256:772dfc9f12cadcf6f85ff524683a4e7573f54415729da2977ab8e555c5058ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325561187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88f3f07586d3b1345665a65f6f029c290e7006136acb1340c4496ac9aaefd20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef025249b0fe621dd5c39de7e56c0ca2be3a550f30946c0103b22cfb65ce0adf`  
		Last Modified: Wed, 05 Jun 2024 04:00:00 GMT  
		Size: 18.2 MB (18222028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909ebbc0bdbd07a40e729bb5b958f22d12e3d154aded190a6cc48e187be81dda`  
		Last Modified: Wed, 24 Jul 2024 04:13:08 GMT  
		Size: 42.7 MB (42652860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f0c163d60b8d17f187a1ce7c28da5c01c3d9a83bde0f609ee802566ab0e06`  
		Last Modified: Wed, 24 Jul 2024 04:13:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faea3162e16d0b444fcf9c459996557e5d1f601adf99cf73c760b8b9878e23b3`  
		Last Modified: Fri, 23 Aug 2024 19:22:59 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58ded00e5023aa126be34126538a4e90e35049e008185370718a123aea1af66`  
		Last Modified: Fri, 27 Sep 2024 01:13:59 GMT  
		Size: 5.9 MB (5940371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5857d29f36440e77a94b7b991b4b98a02ef6a38e9c24c8bdf4c5ccfa8b267c`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 4.3 KB (4284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da4f0c6ee2bd598c44b83fc37ec27923255e7aa8b50bf44d6c3d6c967638463`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5205c994a40e4d1c8c9b615e657ccdc7c748001d58f14ce918028833d94c359f`  
		Last Modified: Fri, 27 Sep 2024 01:14:07 GMT  
		Size: 225.4 MB (225414061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70f48f8e04453528ada753058672d725ef0147cc0943d9eb67d70f5074c9c39`  
		Last Modified: Fri, 27 Sep 2024 01:13:59 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11` - unknown; unknown

```console
$ docker pull solr@sha256:62bb5f0059253f82691951e26d3a3cf21615154b877358973fd6b22f10eb29bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4178856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ac39df8fac4b59e075e61b8327a644ad232e2bc1e0b7c1152dc82a1422db36`

```dockerfile
```

-	Layers:
	-	`sha256:11b6e886a94f119b611024c9ed5c2ec34ba06e8515d89f224753b305838b64f1`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 4.1 MB (4142513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a84dcf1da08de05c4cc25a5562a96fb48c7724ca86e6107a147ecd923098be`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 36.3 KB (36343 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11` - linux; s390x

```console
$ docker pull solr@sha256:f9c59847a1fe3a79da4b53fa9f8533d45a9eb0158af0b014fc86f49d186f7682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314738218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893395ae57b3f59ef1481b44ab1aa5eee040bf4949770070a8885a3c76bd1407`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a156a04bb486c4a1c69c74a9f01dce29f2e013ccab4e6631197f6cc4d8f4c45`  
		Last Modified: Wed, 05 Jun 2024 03:12:17 GMT  
		Size: 16.6 MB (16645456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd37eed98237b35cbfd9c26e61e50843a3e5cd2ebf664c58e31194178944624f`  
		Last Modified: Wed, 24 Jul 2024 00:57:17 GMT  
		Size: 40.8 MB (40818422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6348169ce0d5dbce34a24949a87f35c57f8e5f9d5b1913297de765327f3c20fd`  
		Last Modified: Wed, 24 Jul 2024 00:57:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946104babcd64d4c66119ed87d279d67861c1c2de97404720c98f6ab72c28479`  
		Last Modified: Fri, 23 Aug 2024 19:47:03 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9660b7bfd361d49c9aaf46a8bc5d0c6cfc12cf3f3a5a2b41d79275a772ad9396`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.8 MB (4831179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de1dc16a9b667a45206e90d3b993c443e1ecca9efcc1d2028cc7c19cbb53fee`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548613fbd3494a92c63c875bd3d8d421fe1b0fc893400c1f6a5c13638f930d3d`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8490c3a9d42d5364f6c44f2655ffc8281d3d341cf8f234614a6f845aa90f3fe`  
		Last Modified: Fri, 27 Sep 2024 00:38:02 GMT  
		Size: 225.4 MB (225413966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9931af8cd7f65fb31294e2278dd8819007cb5b6bc05a561e8b4e737189171b5`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11` - unknown; unknown

```console
$ docker pull solr@sha256:3739dbde80f6c36a899ca27963e4a5e54d8fb428f4c310f563cf5e58487f3dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1d143b13416c0df91eb78ec917a934267d6c94a021c6ef3355120c1f1892d6`

```dockerfile
```

-	Layers:
	-	`sha256:7d7205f14935b77276edb09bf5a4f2c0837e9318b83c00cefb02f588cccda61c`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.1 MB (4139433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:456e7de9073c15fd7ed08d73abf6627293e03677d3743c178f57e5693a7f72f2`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 36.3 KB (36306 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:8.11-slim`

```console
$ docker pull solr@sha256:ce41841bc3268ca1b5dd4b67c4b9b18fffce35efdadda479efb78336b76f684a
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
$ docker pull solr@sha256:01c980db779d0405cca055e90f9b565072ef7a64a6a2bef41362019f80408872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.1 MB (323134341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be727de2c22da89cbc0833683bc2f307b4c56bf3e6033a8aca82c49c07de5d12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46bdbd88e5c97485003310b142bf5c3c58bb9677087aed67152e8d6e4d5f47a`  
		Last Modified: Fri, 23 Aug 2024 19:26:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3044a2a9f396b20a6931ca7450fc5f5cf720d6e3fbe0b429cc04587dfb4fbb6a`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 5.0 MB (5002685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d83292bf77153932bf1eaeebd0ceb3031180626dd45af424f532c7ef69ba9f8`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 4.3 KB (4277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d73245baa2d25922e06245c53de062e9ec67c2623518fe4e5afd6e2b8fa60d`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a45605e444e6e20345a76c0b9216f3101d8d1e2421c5883d653960fc35e0e5`  
		Last Modified: Thu, 26 Sep 2024 22:57:19 GMT  
		Size: 225.4 MB (225414058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4ad173f326ed826d2c3d6a42998533c8f43f146e735ccb6410e0510cc8ed1d`  
		Last Modified: Thu, 26 Sep 2024 22:57:17 GMT  
		Size: 6.3 KB (6273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11-slim` - unknown; unknown

```console
$ docker pull solr@sha256:b593d3aa0fd4fc5cba37d26cc5e47df34fe50ad2ff817d7e88397cb4bfe8606f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5f0061d678ecf66773b11a7bcdf5a3e785949db3f7000bc8600a7a0fb26d1d`

```dockerfile
```

-	Layers:
	-	`sha256:a809e5f60af1efff54ce1503161ddde484632f76893b6e03df9ca60539b29df1`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 4.1 MB (4138663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:139d637f919e7b9c2b548536fa87100379bc7c431771406cd8f4ee14a8fb9847`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 36.4 KB (36355 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:f49929f952f41d07353fce812472fff89521e8a08d9a165122e4d5627eff9e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319543360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbfab67d60d3c38eacee040aea03205bf495cbf9ad840f70a001fdea86ebebbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 09 Feb 2024 17:48:20 GMT
ARG RELEASE
# Fri, 09 Feb 2024 17:48:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 09 Feb 2024 17:48:20 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 09 Feb 2024 17:48:20 GMT
CMD ["/bin/bash"]
# Fri, 09 Feb 2024 17:48:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Feb 2024 17:48:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 17:48:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Fri, 09 Feb 2024 17:48:20 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_VERSION=8.11.3
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 09 Feb 2024 17:48:20 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512 # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=https://www.apache.org/dyn/closer.lua/lucene/solr/8.11.3/solr-8.11.3.tgz?action=download SOLR_DIST_URL=https://downloads.apache.org/lucene/solr/8.11.3/solr-8.11.3.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.3/solr-8.11.3.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0 # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME" # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
COPY --chown=0:0 scripts /opt/docker-solr/scripts # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
VOLUME [/var/solr]
# Fri, 09 Feb 2024 17:48:20 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 09 Feb 2024 17:48:20 GMT
WORKDIR /opt/solr
# Fri, 09 Feb 2024 17:48:20 GMT
USER 8983
# Fri, 09 Feb 2024 17:48:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Feb 2024 17:48:20 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba61bfb12e507d61800c2fe5399b1bfd7ee7b2982cfef183447f0d34efdae73e`  
		Last Modified: Wed, 05 Jun 2024 04:54:46 GMT  
		Size: 16.8 MB (16776981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd901b7b2bde002ec1f6b7557a7ce8a3b97f79119ddeefa8519815247c9fd5`  
		Last Modified: Wed, 24 Jul 2024 00:51:39 GMT  
		Size: 45.6 MB (45557235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b215f2e389fbf816c3e9b5264cce0215fe12c76e4d302d2be3ae358b8269d3c`  
		Last Modified: Wed, 24 Jul 2024 00:51:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5a032d75137abf4a646016d6785211957158b7f98ae6bb407f805900f78fc3`  
		Last Modified: Fri, 23 Aug 2024 19:44:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3bd09a8851024db763b997267026cea779ccfb044a389f4b33b4523b80f2da`  
		Last Modified: Sat, 24 Aug 2024 01:17:03 GMT  
		Size: 4.8 MB (4847845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03dc8d97e607d7fac177424ea1a33965f09a1b390b3d9e5783819b8a9b5c77a`  
		Last Modified: Sat, 24 Aug 2024 01:17:02 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fb5486658b2efd5ff1f1a764a3f8e2b30c4e03df4aabb32f4f5d81d67ab759`  
		Last Modified: Sat, 24 Aug 2024 01:17:02 GMT  
		Size: 2.9 KB (2887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1515c20df83019401b79bca95fecac43a6459e851b42a0ae70827e8b8018a50`  
		Last Modified: Sat, 24 Aug 2024 01:17:08 GMT  
		Size: 225.1 MB (225140286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744ef938ef4a607f3c3561a75b5191d336ffdc63517ff3d70336a5c816baf160`  
		Last Modified: Sat, 24 Aug 2024 01:17:03 GMT  
		Size: 6.3 KB (6274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11-slim` - unknown; unknown

```console
$ docker pull solr@sha256:a1ea3e659687e9f8c2b5c7582be7051ef9483172f338eb358ddcfdc7c1223b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4094077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710f0e1aa69f9485eedae4357d82aaf5cc1e1b2a2b315e60626434f853deca7b`

```dockerfile
```

-	Layers:
	-	`sha256:3eaaeb2d1e01fb91bf382d513b72118aa0800dea42a8352457b486b1799eccec`  
		Last Modified: Sat, 24 Aug 2024 01:17:36 GMT  
		Size: 4.1 MB (4057417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e106e70638bc59f5dd76b0ad2d3ecb928934479a70764f7946f0c3b9d5c7f06`  
		Last Modified: Sat, 24 Aug 2024 01:17:36 GMT  
		Size: 36.7 KB (36660 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:4a058c28c45983da0e54185a752c5f50cb72afb1cc063ad306a3e7a952814cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325561187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88f3f07586d3b1345665a65f6f029c290e7006136acb1340c4496ac9aaefd20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef025249b0fe621dd5c39de7e56c0ca2be3a550f30946c0103b22cfb65ce0adf`  
		Last Modified: Wed, 05 Jun 2024 04:00:00 GMT  
		Size: 18.2 MB (18222028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909ebbc0bdbd07a40e729bb5b958f22d12e3d154aded190a6cc48e187be81dda`  
		Last Modified: Wed, 24 Jul 2024 04:13:08 GMT  
		Size: 42.7 MB (42652860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f0c163d60b8d17f187a1ce7c28da5c01c3d9a83bde0f609ee802566ab0e06`  
		Last Modified: Wed, 24 Jul 2024 04:13:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faea3162e16d0b444fcf9c459996557e5d1f601adf99cf73c760b8b9878e23b3`  
		Last Modified: Fri, 23 Aug 2024 19:22:59 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58ded00e5023aa126be34126538a4e90e35049e008185370718a123aea1af66`  
		Last Modified: Fri, 27 Sep 2024 01:13:59 GMT  
		Size: 5.9 MB (5940371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5857d29f36440e77a94b7b991b4b98a02ef6a38e9c24c8bdf4c5ccfa8b267c`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 4.3 KB (4284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da4f0c6ee2bd598c44b83fc37ec27923255e7aa8b50bf44d6c3d6c967638463`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5205c994a40e4d1c8c9b615e657ccdc7c748001d58f14ce918028833d94c359f`  
		Last Modified: Fri, 27 Sep 2024 01:14:07 GMT  
		Size: 225.4 MB (225414061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70f48f8e04453528ada753058672d725ef0147cc0943d9eb67d70f5074c9c39`  
		Last Modified: Fri, 27 Sep 2024 01:13:59 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11-slim` - unknown; unknown

```console
$ docker pull solr@sha256:ff8f1ee348694d97e824badb92b4b34480e3368725edae8d1d906a6ea600c653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4178936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcb2a16ef989a3435c7db236ab60442092b0c89303b3ffcb18203c64b77f528`

```dockerfile
```

-	Layers:
	-	`sha256:c5dcbd5ecdaa07abcc20069025e065bab53521264cc5edfd56094fbd6273316d`  
		Last Modified: Fri, 27 Sep 2024 01:14:55 GMT  
		Size: 4.1 MB (4142543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d17b39e08c4502d5db7d1a69143163b1bd21d32e35baa28294ba619c7cd3ed7`  
		Last Modified: Fri, 27 Sep 2024 01:14:54 GMT  
		Size: 36.4 KB (36393 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11-slim` - linux; s390x

```console
$ docker pull solr@sha256:e3fdde108d6bc2c4f8625650c8fe0a426248232a32ac0e5bb387598d1c27ec97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314738218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893395ae57b3f59ef1481b44ab1aa5eee040bf4949770070a8885a3c76bd1407`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a156a04bb486c4a1c69c74a9f01dce29f2e013ccab4e6631197f6cc4d8f4c45`  
		Last Modified: Wed, 05 Jun 2024 03:12:17 GMT  
		Size: 16.6 MB (16645456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd37eed98237b35cbfd9c26e61e50843a3e5cd2ebf664c58e31194178944624f`  
		Last Modified: Wed, 24 Jul 2024 00:57:17 GMT  
		Size: 40.8 MB (40818422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6348169ce0d5dbce34a24949a87f35c57f8e5f9d5b1913297de765327f3c20fd`  
		Last Modified: Wed, 24 Jul 2024 00:57:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946104babcd64d4c66119ed87d279d67861c1c2de97404720c98f6ab72c28479`  
		Last Modified: Fri, 23 Aug 2024 19:47:03 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9660b7bfd361d49c9aaf46a8bc5d0c6cfc12cf3f3a5a2b41d79275a772ad9396`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.8 MB (4831179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de1dc16a9b667a45206e90d3b993c443e1ecca9efcc1d2028cc7c19cbb53fee`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548613fbd3494a92c63c875bd3d8d421fe1b0fc893400c1f6a5c13638f930d3d`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8490c3a9d42d5364f6c44f2655ffc8281d3d341cf8f234614a6f845aa90f3fe`  
		Last Modified: Fri, 27 Sep 2024 00:38:02 GMT  
		Size: 225.4 MB (225413966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9931af8cd7f65fb31294e2278dd8819007cb5b6bc05a561e8b4e737189171b5`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11-slim` - unknown; unknown

```console
$ docker pull solr@sha256:bfe99b6c2a89bae7413e4cab75a5d1929a5e92ea052dfee84157732d24f8d2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b9697ba081a8fc94b54777b7e167a98651e24aa8b1340e6bca057bef5c01a1`

```dockerfile
```

-	Layers:
	-	`sha256:066325287907bb4fa898d3b1a6e296e8c961f2e78bff52008c1b869c41572a39`  
		Last Modified: Fri, 27 Sep 2024 00:38:47 GMT  
		Size: 4.1 MB (4139463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60e102343a5d9563aef8ea32fdc4299b94b4a3086b2c9f3ca08587be8add80a1`  
		Last Modified: Fri, 27 Sep 2024 00:38:47 GMT  
		Size: 36.4 KB (36355 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:8.11.4`

```console
$ docker pull solr@sha256:87ba85b932ac0a2e6b16908310370463f6b1be6df4b49d98863051c356566eab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `solr:8.11.4` - linux; amd64

```console
$ docker pull solr@sha256:c5d27cb1a075801217cc7463bbca9725943a2186bc61062cc999f010bdcc4d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.1 MB (323134323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:defb8f5bfd3bbf979184e306d510eac3baef5e8a6d72d0e67741e76aaebe565b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46bdbd88e5c97485003310b142bf5c3c58bb9677087aed67152e8d6e4d5f47a`  
		Last Modified: Fri, 23 Aug 2024 19:26:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7efbf9e7d7c55fd4a7d7cf86817e5dc3128427e806a1576d8ddb50d04f937`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 5.0 MB (5002678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0454dc334683a867cfdf81593cd7b353df482767a2efeb2223d43c19c3fe9ed`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a486d837e8bce146166479fe29d4f1d4cd0a87fa3c5ae95ed711432f1a95fbff`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 2.9 KB (2887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5c31765272d843b81a4a150390c4f9e150f075e04eca5d675ab639be77f7ea`  
		Last Modified: Thu, 26 Sep 2024 22:57:19 GMT  
		Size: 225.4 MB (225414053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edff86e4fdd655e5933db69bd0dd6268deceb49d51b11ca70e200fe7fc2cac4`  
		Last Modified: Thu, 26 Sep 2024 22:57:17 GMT  
		Size: 6.3 KB (6271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11.4` - unknown; unknown

```console
$ docker pull solr@sha256:84507e96b4ccd30467dba7b3effe3dadf152d4c2043b728f481708d459907eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4174939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37de412a80c202573995c9e9279c78eed6abb7ac93deb38a7993b33b0b2af5f6`

```dockerfile
```

-	Layers:
	-	`sha256:12880be67fb3782d6d958b78721173d27e737948a2a63f920dbc1947ac53178f`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 4.1 MB (4138633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef11850f7f236d2edb6deaadc40dae95ba4cd13ade40a89e03c07c3692725eb5`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 36.3 KB (36306 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11.4` - linux; ppc64le

```console
$ docker pull solr@sha256:772dfc9f12cadcf6f85ff524683a4e7573f54415729da2977ab8e555c5058ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325561187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88f3f07586d3b1345665a65f6f029c290e7006136acb1340c4496ac9aaefd20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef025249b0fe621dd5c39de7e56c0ca2be3a550f30946c0103b22cfb65ce0adf`  
		Last Modified: Wed, 05 Jun 2024 04:00:00 GMT  
		Size: 18.2 MB (18222028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909ebbc0bdbd07a40e729bb5b958f22d12e3d154aded190a6cc48e187be81dda`  
		Last Modified: Wed, 24 Jul 2024 04:13:08 GMT  
		Size: 42.7 MB (42652860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f0c163d60b8d17f187a1ce7c28da5c01c3d9a83bde0f609ee802566ab0e06`  
		Last Modified: Wed, 24 Jul 2024 04:13:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faea3162e16d0b444fcf9c459996557e5d1f601adf99cf73c760b8b9878e23b3`  
		Last Modified: Fri, 23 Aug 2024 19:22:59 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58ded00e5023aa126be34126538a4e90e35049e008185370718a123aea1af66`  
		Last Modified: Fri, 27 Sep 2024 01:13:59 GMT  
		Size: 5.9 MB (5940371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5857d29f36440e77a94b7b991b4b98a02ef6a38e9c24c8bdf4c5ccfa8b267c`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 4.3 KB (4284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da4f0c6ee2bd598c44b83fc37ec27923255e7aa8b50bf44d6c3d6c967638463`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5205c994a40e4d1c8c9b615e657ccdc7c748001d58f14ce918028833d94c359f`  
		Last Modified: Fri, 27 Sep 2024 01:14:07 GMT  
		Size: 225.4 MB (225414061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70f48f8e04453528ada753058672d725ef0147cc0943d9eb67d70f5074c9c39`  
		Last Modified: Fri, 27 Sep 2024 01:13:59 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11.4` - unknown; unknown

```console
$ docker pull solr@sha256:62bb5f0059253f82691951e26d3a3cf21615154b877358973fd6b22f10eb29bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4178856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ac39df8fac4b59e075e61b8327a644ad232e2bc1e0b7c1152dc82a1422db36`

```dockerfile
```

-	Layers:
	-	`sha256:11b6e886a94f119b611024c9ed5c2ec34ba06e8515d89f224753b305838b64f1`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 4.1 MB (4142513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a84dcf1da08de05c4cc25a5562a96fb48c7724ca86e6107a147ecd923098be`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 36.3 KB (36343 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11.4` - linux; s390x

```console
$ docker pull solr@sha256:f9c59847a1fe3a79da4b53fa9f8533d45a9eb0158af0b014fc86f49d186f7682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314738218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893395ae57b3f59ef1481b44ab1aa5eee040bf4949770070a8885a3c76bd1407`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a156a04bb486c4a1c69c74a9f01dce29f2e013ccab4e6631197f6cc4d8f4c45`  
		Last Modified: Wed, 05 Jun 2024 03:12:17 GMT  
		Size: 16.6 MB (16645456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd37eed98237b35cbfd9c26e61e50843a3e5cd2ebf664c58e31194178944624f`  
		Last Modified: Wed, 24 Jul 2024 00:57:17 GMT  
		Size: 40.8 MB (40818422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6348169ce0d5dbce34a24949a87f35c57f8e5f9d5b1913297de765327f3c20fd`  
		Last Modified: Wed, 24 Jul 2024 00:57:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946104babcd64d4c66119ed87d279d67861c1c2de97404720c98f6ab72c28479`  
		Last Modified: Fri, 23 Aug 2024 19:47:03 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9660b7bfd361d49c9aaf46a8bc5d0c6cfc12cf3f3a5a2b41d79275a772ad9396`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.8 MB (4831179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de1dc16a9b667a45206e90d3b993c443e1ecca9efcc1d2028cc7c19cbb53fee`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548613fbd3494a92c63c875bd3d8d421fe1b0fc893400c1f6a5c13638f930d3d`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8490c3a9d42d5364f6c44f2655ffc8281d3d341cf8f234614a6f845aa90f3fe`  
		Last Modified: Fri, 27 Sep 2024 00:38:02 GMT  
		Size: 225.4 MB (225413966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9931af8cd7f65fb31294e2278dd8819007cb5b6bc05a561e8b4e737189171b5`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11.4` - unknown; unknown

```console
$ docker pull solr@sha256:3739dbde80f6c36a899ca27963e4a5e54d8fb428f4c310f563cf5e58487f3dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1d143b13416c0df91eb78ec917a934267d6c94a021c6ef3355120c1f1892d6`

```dockerfile
```

-	Layers:
	-	`sha256:7d7205f14935b77276edb09bf5a4f2c0837e9318b83c00cefb02f588cccda61c`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.1 MB (4139433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:456e7de9073c15fd7ed08d73abf6627293e03677d3743c178f57e5693a7f72f2`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 36.3 KB (36306 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:8.11.4-slim`

```console
$ docker pull solr@sha256:fd036cba0a8c4eb6987c17d101dcb377c578654049185778f0a4c2cf8d50c675
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `solr:8.11.4-slim` - linux; amd64

```console
$ docker pull solr@sha256:01c980db779d0405cca055e90f9b565072ef7a64a6a2bef41362019f80408872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.1 MB (323134341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be727de2c22da89cbc0833683bc2f307b4c56bf3e6033a8aca82c49c07de5d12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46bdbd88e5c97485003310b142bf5c3c58bb9677087aed67152e8d6e4d5f47a`  
		Last Modified: Fri, 23 Aug 2024 19:26:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3044a2a9f396b20a6931ca7450fc5f5cf720d6e3fbe0b429cc04587dfb4fbb6a`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 5.0 MB (5002685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d83292bf77153932bf1eaeebd0ceb3031180626dd45af424f532c7ef69ba9f8`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 4.3 KB (4277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d73245baa2d25922e06245c53de062e9ec67c2623518fe4e5afd6e2b8fa60d`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a45605e444e6e20345a76c0b9216f3101d8d1e2421c5883d653960fc35e0e5`  
		Last Modified: Thu, 26 Sep 2024 22:57:19 GMT  
		Size: 225.4 MB (225414058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4ad173f326ed826d2c3d6a42998533c8f43f146e735ccb6410e0510cc8ed1d`  
		Last Modified: Thu, 26 Sep 2024 22:57:17 GMT  
		Size: 6.3 KB (6273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11.4-slim` - unknown; unknown

```console
$ docker pull solr@sha256:b593d3aa0fd4fc5cba37d26cc5e47df34fe50ad2ff817d7e88397cb4bfe8606f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5f0061d678ecf66773b11a7bcdf5a3e785949db3f7000bc8600a7a0fb26d1d`

```dockerfile
```

-	Layers:
	-	`sha256:a809e5f60af1efff54ce1503161ddde484632f76893b6e03df9ca60539b29df1`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 4.1 MB (4138663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:139d637f919e7b9c2b548536fa87100379bc7c431771406cd8f4ee14a8fb9847`  
		Last Modified: Thu, 26 Sep 2024 22:57:16 GMT  
		Size: 36.4 KB (36355 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11.4-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:4a058c28c45983da0e54185a752c5f50cb72afb1cc063ad306a3e7a952814cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325561187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88f3f07586d3b1345665a65f6f029c290e7006136acb1340c4496ac9aaefd20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef025249b0fe621dd5c39de7e56c0ca2be3a550f30946c0103b22cfb65ce0adf`  
		Last Modified: Wed, 05 Jun 2024 04:00:00 GMT  
		Size: 18.2 MB (18222028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909ebbc0bdbd07a40e729bb5b958f22d12e3d154aded190a6cc48e187be81dda`  
		Last Modified: Wed, 24 Jul 2024 04:13:08 GMT  
		Size: 42.7 MB (42652860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f0c163d60b8d17f187a1ce7c28da5c01c3d9a83bde0f609ee802566ab0e06`  
		Last Modified: Wed, 24 Jul 2024 04:13:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faea3162e16d0b444fcf9c459996557e5d1f601adf99cf73c760b8b9878e23b3`  
		Last Modified: Fri, 23 Aug 2024 19:22:59 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58ded00e5023aa126be34126538a4e90e35049e008185370718a123aea1af66`  
		Last Modified: Fri, 27 Sep 2024 01:13:59 GMT  
		Size: 5.9 MB (5940371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5857d29f36440e77a94b7b991b4b98a02ef6a38e9c24c8bdf4c5ccfa8b267c`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 4.3 KB (4284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da4f0c6ee2bd598c44b83fc37ec27923255e7aa8b50bf44d6c3d6c967638463`  
		Last Modified: Fri, 27 Sep 2024 01:13:58 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5205c994a40e4d1c8c9b615e657ccdc7c748001d58f14ce918028833d94c359f`  
		Last Modified: Fri, 27 Sep 2024 01:14:07 GMT  
		Size: 225.4 MB (225414061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70f48f8e04453528ada753058672d725ef0147cc0943d9eb67d70f5074c9c39`  
		Last Modified: Fri, 27 Sep 2024 01:13:59 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11.4-slim` - unknown; unknown

```console
$ docker pull solr@sha256:ff8f1ee348694d97e824badb92b4b34480e3368725edae8d1d906a6ea600c653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4178936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcb2a16ef989a3435c7db236ab60442092b0c89303b3ffcb18203c64b77f528`

```dockerfile
```

-	Layers:
	-	`sha256:c5dcbd5ecdaa07abcc20069025e065bab53521264cc5edfd56094fbd6273316d`  
		Last Modified: Fri, 27 Sep 2024 01:14:55 GMT  
		Size: 4.1 MB (4142543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d17b39e08c4502d5db7d1a69143163b1bd21d32e35baa28294ba619c7cd3ed7`  
		Last Modified: Fri, 27 Sep 2024 01:14:54 GMT  
		Size: 36.4 KB (36393 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8.11.4-slim` - linux; s390x

```console
$ docker pull solr@sha256:e3fdde108d6bc2c4f8625650c8fe0a426248232a32ac0e5bb387598d1c27ec97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314738218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893395ae57b3f59ef1481b44ab1aa5eee040bf4949770070a8885a3c76bd1407`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a156a04bb486c4a1c69c74a9f01dce29f2e013ccab4e6631197f6cc4d8f4c45`  
		Last Modified: Wed, 05 Jun 2024 03:12:17 GMT  
		Size: 16.6 MB (16645456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd37eed98237b35cbfd9c26e61e50843a3e5cd2ebf664c58e31194178944624f`  
		Last Modified: Wed, 24 Jul 2024 00:57:17 GMT  
		Size: 40.8 MB (40818422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6348169ce0d5dbce34a24949a87f35c57f8e5f9d5b1913297de765327f3c20fd`  
		Last Modified: Wed, 24 Jul 2024 00:57:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946104babcd64d4c66119ed87d279d67861c1c2de97404720c98f6ab72c28479`  
		Last Modified: Fri, 23 Aug 2024 19:47:03 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9660b7bfd361d49c9aaf46a8bc5d0c6cfc12cf3f3a5a2b41d79275a772ad9396`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.8 MB (4831179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de1dc16a9b667a45206e90d3b993c443e1ecca9efcc1d2028cc7c19cbb53fee`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548613fbd3494a92c63c875bd3d8d421fe1b0fc893400c1f6a5c13638f930d3d`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8490c3a9d42d5364f6c44f2655ffc8281d3d341cf8f234614a6f845aa90f3fe`  
		Last Modified: Fri, 27 Sep 2024 00:38:02 GMT  
		Size: 225.4 MB (225413966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9931af8cd7f65fb31294e2278dd8819007cb5b6bc05a561e8b4e737189171b5`  
		Last Modified: Fri, 27 Sep 2024 00:37:54 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8.11.4-slim` - unknown; unknown

```console
$ docker pull solr@sha256:bfe99b6c2a89bae7413e4cab75a5d1929a5e92ea052dfee84157732d24f8d2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b9697ba081a8fc94b54777b7e167a98651e24aa8b1340e6bca057bef5c01a1`

```dockerfile
```

-	Layers:
	-	`sha256:066325287907bb4fa898d3b1a6e296e8c961f2e78bff52008c1b869c41572a39`  
		Last Modified: Fri, 27 Sep 2024 00:38:47 GMT  
		Size: 4.1 MB (4139463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60e102343a5d9563aef8ea32fdc4299b94b4a3086b2c9f3ca08587be8add80a1`  
		Last Modified: Fri, 27 Sep 2024 00:38:47 GMT  
		Size: 36.4 KB (36355 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9`

```console
$ docker pull solr@sha256:4267344d8d37c5982894f8424e923a66e21461fc2d61602d935837d5d464182b
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
$ docker pull solr@sha256:c56b658c959f8ad2b7389d9b0107b48e3f95f13419788300f1f1297f198abdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.3 MB (375281077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d0bd9e56bc994ea086b4d7169937de4f8db32e98b1d481b13ec19856ebf830`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1aa583d1ef98fcaf42e21c147c70dd631fa34b36dc593c64265c54921dfd03`  
		Last Modified: Tue, 17 Sep 2024 01:58:19 GMT  
		Size: 283.1 MB (283083900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350cf53fd52a58d48f5d69688ffa4f77f51394ce81c3e6e81cb986dc1bba540d`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 4.3 KB (4270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b317c36e5a1025abf32228209e48b34ad153043e1bf9998c560e0b6e4e727164`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf7dd409191fcd1d9d51f54e8bfabeb0a53eca08b8da688a07588992f36b52c`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 10.9 KB (10867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24483e359719eee7ece7e8523546cd960c86efecf9b6990a080cbfdeb511ed1`  
		Last Modified: Tue, 17 Sep 2024 01:58:16 GMT  
		Size: 1.6 MB (1588536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:116ea6808bd356110ff347fb2574c286b721260a361f2e4ce35c6c678805e065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf593f0ad90c7de914051d98bb6b2ddf483c741f512f5d6842d0cc84b6e2af44`

```dockerfile
```

-	Layers:
	-	`sha256:77ffd5df8f3b12549b2e1216fd01df2f73b62374c87491ce014674f558833868`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 4.2 MB (4150903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c21b111477b68635e4f4ae71603feb8b8130a7feb123ba9b0d691d17b3ee7c55`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 34.0 KB (34047 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:4ceca4ac998615dc3a80f7e67cf92dbd847e8e0bc04237f6f9f2928e75e82882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.5 MB (372505844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1026faf3194f8160c949410787ea9ffedf89e75772f25ecded9856195b0628e3`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257dbd9b6c377e0e75f4fe02716f6f373ee72cb589786a680f1100c695eaeb7a`  
		Last Modified: Tue, 17 Sep 2024 06:19:49 GMT  
		Size: 283.1 MB (283084078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f21f0a74e3bbc74b2541e017928f67aa6d3a04761bcf33faea7de058243d2c`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c12824d064498f7b2618f5c761d37409e87c6988cbc3b467b4c7f97e11fc5a1`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3aecd7313dcf51494ca18f98fb241d436e70d7b029239ba20b93d3d3d489b6`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 10.9 KB (10866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779e44c15834a5a622a574b87658e1eea3fe44616ee17308d5913942c21143fb`  
		Last Modified: Tue, 17 Sep 2024 06:19:45 GMT  
		Size: 1.4 MB (1447466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:e0a29761c26bec3ef130ef5c7d2d315ce715b0d10adaf2d1b1f01bd83b8c323a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4185560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d057f70f18b40b0e4d653edffbca453948a50642e3b3b73f3152c6e4785a342f`

```dockerfile
```

-	Layers:
	-	`sha256:0212511128601e44c88cca991fabc909ad9628577f68ee3d509facdb93f12d04`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 4.2 MB (4151196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b27012cb6170b8ae603f9c2a10a700f3e3b886e6ffcc9626104a9fb3fdb6481`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 34.4 KB (34364 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9` - linux; ppc64le

```console
$ docker pull solr@sha256:8b600bef8663026dc5874367d43a9c3b59236b3c75318ce6373ee4a2c20136eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381114029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09b1467a0770309e9acfdcac3b31cde50317cb57fb054cafc3e84e743017018`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2709165c356fd5bb9b4cda23232d8784bb71b95b05f605dc769df016474e33`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.1 MB (47115977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc5fce86e3a84ba35d6a9f9a976bd027569095ac890bb0a9be084a7b6d46a8e`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0e5434baa9330313b9e3fe8158f7e429b8e6f670f7827e3d0b7bf783db8f5`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9166f7814dcdbd5edcd0d198132f7d73400d07b553026275a8342b616828d4`  
		Last Modified: Tue, 17 Sep 2024 04:18:51 GMT  
		Size: 283.1 MB (283084447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fa47877401d2d997531c42aef453f1eedc981d83852613e4ffca8477d4dfc8`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 4.3 KB (4272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d41a688a4887ac1150669945f16640ce2f3ac7cf475e467466c3ef6a1c93388`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c4bd764cd9f26217ca67a27b61282e8017b5aacf46c492a07431fecbd6a45e`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 10.9 KB (10869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e3bd936391e4c95488f614d045b4a5051908e7a29245e0843e46cb0bbac3ba`  
		Last Modified: Tue, 17 Sep 2024 04:18:37 GMT  
		Size: 1.6 MB (1595531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:59588f3a8c982f85ce93be7a1d83ee2ecdc7d792b86d2e0eeff44ad435bdd32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953461ab2f2864fe202fd7a6d9870b694ab1e34170ea32e106993b64fe26425f`

```dockerfile
```

-	Layers:
	-	`sha256:6c494bbe8b57e7dd6714c1808135ff95ab2809e144769c06eddedf7bebae47ba`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 4.2 MB (4155429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e059d40138e1cee3c2b194f47ce62337b83272ba72e5d47b87ab59fbcf2f1e7a`  
		Last Modified: Tue, 17 Sep 2024 04:18:35 GMT  
		Size: 34.1 KB (34093 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9` - linux; s390x

```console
$ docker pull solr@sha256:0bd26f3815d4fbefdbc761da39c01cd601d74ee2b09555e49dc96d107fcbe1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370095765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3da1f9242c39468fe09d3e3fc38d13b71ff16f3bb82a6267fc404c9384f1c85`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd33900eddbaad7aef6f3b868400a94709edd5e4d439c0e7bf926ca7c34f184`  
		Last Modified: Tue, 17 Sep 2024 03:49:44 GMT  
		Size: 283.1 MB (283084224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d394f36e696d6e8145c7a7e05e50accc945e8347475575e3f8f3689b66646c8`  
		Last Modified: Tue, 17 Sep 2024 03:49:38 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b9a8d32862a02e8f90876527c50eea0d08b003a77bc1ed996341d57c4a206b`  
		Last Modified: Tue, 17 Sep 2024 03:49:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338736aa5b5c8d8c26d0208cd61c557a4ff9296d102001a445c72e802fcf10b6`  
		Last Modified: Tue, 17 Sep 2024 03:49:39 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95b165658950bff630dcbbedda6c18c58b3f786eda04774cd52c499e8b450ef`  
		Last Modified: Tue, 17 Sep 2024 03:49:40 GMT  
		Size: 1.5 MB (1535227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9` - unknown; unknown

```console
$ docker pull solr@sha256:077ce584ebc58a06dd0bfdd36085167a7b6e1c793ab986888f63446ca1cbd65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68118e13fe2e2840d191ff87b4cabfcf096b2764a3283fff584131964ae760c`

```dockerfile
```

-	Layers:
	-	`sha256:34f5f352acf6521c285cff397e1c9b7d735f1273e2a3d5e0455465e3a3974b1c`  
		Last Modified: Tue, 17 Sep 2024 03:49:39 GMT  
		Size: 4.2 MB (4152024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ecb0590de35c286840f10eeb7146a800dd09d72372f788ec9ea620e04b3319`  
		Last Modified: Tue, 17 Sep 2024 03:49:38 GMT  
		Size: 34.0 KB (34047 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9-slim`

```console
$ docker pull solr@sha256:3191833409ac0349ebea8c9da9f2c8a0633ca67b184aeb1a36902e9b5d38539b
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
$ docker pull solr@sha256:5ff61de1418757425e028737bd010cb2a030b7a1955b8b9eea5de16a40f9ee9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157019263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb6986494c44f94ddfff0d1548a447d8fb79b7ecfa3559d8b2ccebc753753ea`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018cda53b3efa90b157c23cc92e3b69774f056abb446134fcbe3d15968857f5b`  
		Last Modified: Tue, 17 Sep 2024 01:58:08 GMT  
		Size: 64.8 MB (64822172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08103616a43c638c607be5d934ef046dc7bf8892966d0d961410f521e5a408f`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf3eabf6b02922222663f92fc056535dd5cd97dffb88684cfada2c309d3e9a5`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2fdc48848131a85389028e210f9f91b785eb6da8e2b928aebfa41cfab8261`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 10.8 KB (10782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec4a377ac5fd8f8ad2701146a5a77a47c863cc86c49c33b7028e3f178227759`  
		Last Modified: Tue, 17 Sep 2024 01:58:07 GMT  
		Size: 1.6 MB (1588526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:7c01207568df7fdc13030f0e12715086f630e571609daa9f21c3bf1109809bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe29adbd3d3ea2cf6b3227d2161d33bcd0cfda642f758da5a8ba5db7b05bd00`

```dockerfile
```

-	Layers:
	-	`sha256:2220b180518a4ec4985d4aba0ce5f4709142a2e133ffe6c9f51724b30f086261`  
		Last Modified: Tue, 17 Sep 2024 01:58:06 GMT  
		Size: 3.7 MB (3706729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43757148e05e2334fb7b85597007c07bc672e833ed833c9be2de45452ca9f8db`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:195777fdbe8279808802bb4c2ff7b1041272f518a0f9159a332ff16d5a51f159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154244158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b542ab37706376e5ec336fe0a9b6b4caaaa37d4871b6e5056bd36db6068a3`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3acf7c85b7b1f4080586a56569199ed6f2666a97848ddf34af9b4e293115625`  
		Last Modified: Tue, 17 Sep 2024 06:20:40 GMT  
		Size: 64.8 MB (64822511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba76d9fa57a3a819707684b72833bd5aeefe6fc85ff3381d8e70dad81be1f757`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873080c20f3d3b7bdd26193c8dc28a1fd8e59f1bcbfdd76466cb23275c14d058`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630bf46d6ed4ff01c66668d72efe9a5a16e8687f695b1bc9d7b149102c059bfd`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 10.8 KB (10784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4d80fe3aa5c186c73106441598d6eb763e63207fbc6239f7dcb3a1224a3ce6`  
		Last Modified: Tue, 17 Sep 2024 06:20:40 GMT  
		Size: 1.4 MB (1447434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:97407c4de63b8e01b224ee43dd35888e107b73681c837cfa38244c92b6658873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525e5ee236c9c5a45c300ce639ed98156bce968bdf4ca90be36f6fc7c6b5b414`

```dockerfile
```

-	Layers:
	-	`sha256:feee39d2f9c4621a59b06a62cfc026ac84f2fd59fe467da055d5a4896f295df3`  
		Last Modified: Tue, 17 Sep 2024 06:20:39 GMT  
		Size: 3.7 MB (3707022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f5788cdf11a8e7fc232a9a7e986fee1e36af56c55e911982d495c24dbdc12d`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:e474e41543c8a0f9d6c112656b3bc26c5ded6e7c7c877387fa247afe2dfdb728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162852273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cd1f1da329fdff8aa31f379d00d1a5f5f98a22361697b9188e7dcb7edc4641`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2709165c356fd5bb9b4cda23232d8784bb71b95b05f605dc769df016474e33`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.1 MB (47115977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc5fce86e3a84ba35d6a9f9a976bd027569095ac890bb0a9be084a7b6d46a8e`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0e5434baa9330313b9e3fe8158f7e429b8e6f670f7827e3d0b7bf783db8f5`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5cc63a136204177cb009444f1d4e30f778fa6342bc1fff3c415a2db26af859`  
		Last Modified: Tue, 17 Sep 2024 04:20:10 GMT  
		Size: 64.8 MB (64822807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f015af6089a3d3ce9ea59d066d6e2dfb91c3d75c469700392340d72a2cd9fb3`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 4.3 KB (4271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545d733fba4628b2bd6eac8273fb73a70b5ba52a64d8d929b83ecd8c6db0abba`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28954cd8d780db42f4455b9cd967947a7ccb6d8d238ae02092fa47cf80f3979f`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 10.8 KB (10787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c02cb793eafe46508fca732577230f3775f580de6283a3bef2bf557b2042a1`  
		Last Modified: Tue, 17 Sep 2024 04:20:09 GMT  
		Size: 1.6 MB (1595495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1e6d3fd4742692de1a98951978739b1424a65b1aacc6ae0274ee4c78aa185510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6632a300c80447bf453aa8a2d18ab3da903a6f2edd8f2fa73b4338503bab3d6`

```dockerfile
```

-	Layers:
	-	`sha256:466e5869a02f90160dd4ace6559b190ce24b3e1170f4b5245be5b7519f80dd99`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 3.7 MB (3711255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ec45fb6fec772aafb9e7bb001461fd296b07e2640a8da505888d788eaa2e4b`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 34.2 KB (34154 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; s390x

```console
$ docker pull solr@sha256:32aed8931be1df5fa8a4162fe06a48d6201aafb1ba297d28892987e501c8a5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151834055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a35a7e1018908896a4c1af9b4756ce7e9636fcb1561c19f630b9dd5a66a2c30`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2e4d148efe9b8ddc93fd95944cfa339847af273a2c1670177a272b9c577e49`  
		Last Modified: Tue, 17 Sep 2024 03:50:40 GMT  
		Size: 64.8 MB (64822613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de244efe4184c250f4ce53ad165d6e71af82b7a2d23601aefb5a7a5e2a08c098`  
		Last Modified: Tue, 17 Sep 2024 03:50:38 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75870b73c63df3e5916f4b20f3323eed537098164758505af69724e3eefe9b`  
		Last Modified: Tue, 17 Sep 2024 03:50:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dcf24f699c68c7dec74826b6f70798ec436579e1f7dd06eaaa1a8cf3cfe35a`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 10.8 KB (10784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319ac3aec22f66e31b317e2d05576e041647c7aa97cddc869c9a91a8366ef6d`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 1.5 MB (1535216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:fac442f0523e1bb9886faace4e58d3b7cbc0683098f3de217f52c081df815a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b4502bc0be4c2e4b593a45180e288d60412f833f088ed4d31945adf507f055`

```dockerfile
```

-	Layers:
	-	`sha256:20273b8ec3e4c6442e0a5008f3f9ad0431185cd634d1d878c141a9574300d6e2`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 3.7 MB (3707850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8923fe4b3af6f27a6fae4be88118b6f5bbf9e79e928395bc3d20b86f013ac06`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.6`

```console
$ docker pull solr@sha256:21aa3ccfc2dcd1365dd84e23798c8755f16d936e42d767f7ba65c298ef14891d
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

### `solr:9.6` - linux; amd64

```console
$ docker pull solr@sha256:eb81e5e1aa2b0a24cdfce10002e04738c15e5493b34ea61d8ffbfa5e145ecff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.9 MB (374854880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5606750d95b24167dd5a2300936a4efd18655a050726dd6b745bc712b0b19840`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee6ff2cba794811e53bd23f5d7e7f4b587421632b8e25ca1e65c97ae1003e41`  
		Last Modified: Tue, 17 Sep 2024 02:00:51 GMT  
		Size: 282.7 MB (282657709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b4af993082e9b9234927f53528aed82fdb52b4682dc15d91a5d0289ddc57d`  
		Last Modified: Tue, 17 Sep 2024 02:00:44 GMT  
		Size: 4.3 KB (4269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfc8d8a4b67f139a87f9dd28c07e1ef53024776af8f665a5bf4d7d47c354710`  
		Last Modified: Tue, 17 Sep 2024 02:00:44 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433f5b970a160ef67e0ec69d75118b99ee9233a7e4292b088fba071ec0c8a32b`  
		Last Modified: Tue, 17 Sep 2024 02:00:44 GMT  
		Size: 10.9 KB (10870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025719eb0bae9901858e2be995667919d14c7075f6cee07b8424d72344b37f1a`  
		Last Modified: Tue, 17 Sep 2024 02:00:46 GMT  
		Size: 1.6 MB (1588525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6` - unknown; unknown

```console
$ docker pull solr@sha256:aa7ed4bad7856d7853ae4d8cdc89394be4b5c22dc3d7f8f02b4dbbdd9128b21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4163462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e6be1fcf1c318e73a5808c280041e5798c86d2b417ae5d04ea1dce8d6e1507`

```dockerfile
```

-	Layers:
	-	`sha256:74f32183e5315da7b171e393eae2a693ac19fb1b7aa53b91f91bb682e3d5ac09`  
		Last Modified: Tue, 17 Sep 2024 02:00:45 GMT  
		Size: 4.1 MB (4129993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2385ae3be093cb067dd65dd88fce7a35909d83243eb6013db4fb903ef4c05baf`  
		Last Modified: Tue, 17 Sep 2024 02:00:44 GMT  
		Size: 33.5 KB (33469 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.6` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:e70271df54957f08f0bbcc8262b35bde86652dcc2799aa5479f3147f49668bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.1 MB (372079616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba793ebde9e3034a55209bc053a019ef3b007b3facaa57253d3184b804db1262`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed8e54022b4dd9c5d0c209217dcf58d4b3a44b51e0e5dbd6fef3750de645adc`  
		Last Modified: Tue, 17 Sep 2024 06:22:08 GMT  
		Size: 282.7 MB (282657893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ef56b6938a107d06eba1cb1f1af513128b0aaaee112de6adaab995cb8d519f`  
		Last Modified: Tue, 17 Sep 2024 06:22:00 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2848e3662dfcd73d5567bf2154dbb89db8c8497e4646ff0d8ef61d9862c607e8`  
		Last Modified: Tue, 17 Sep 2024 06:22:00 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c269f24ca86ff9ce654e5060a73c56225782c2ac869261f5651aa2083b0860`  
		Last Modified: Tue, 17 Sep 2024 06:22:00 GMT  
		Size: 10.9 KB (10868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69814293d747ca42cd11b1080b8ee13e7cfb653e8f24030b24e88dd20987166c`  
		Last Modified: Tue, 17 Sep 2024 06:22:01 GMT  
		Size: 1.4 MB (1447424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6` - unknown; unknown

```console
$ docker pull solr@sha256:17da78638eef92203746cd654e1fc9a7dc6388cd89a7a14c89617ed725b78cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4164024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310f7530e445b1015ed07e82ae070fd74469c79c4f20d25d235904b52b56ae85`

```dockerfile
```

-	Layers:
	-	`sha256:a8a987b553496f672fe6bd20eb7bcd6411a8156a94b93870098c9c8fee599b7f`  
		Last Modified: Tue, 17 Sep 2024 06:22:00 GMT  
		Size: 4.1 MB (4130262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f19f59ab6c50b79aaab071bebd06fcb8901351e93dd95dab171ebc3c2bbae583`  
		Last Modified: Tue, 17 Sep 2024 06:21:59 GMT  
		Size: 33.8 KB (33762 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.6` - linux; ppc64le

```console
$ docker pull solr@sha256:12c3311761e780d32afcfadc82231bd36fc84155ba2b9eee980fa2ee00fe182f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380687925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457e05e485b18d9edbe78b48c2a5e26c74bc3bbf69fc874c777bf6ced25c9696`
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
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2709165c356fd5bb9b4cda23232d8784bb71b95b05f605dc769df016474e33`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.1 MB (47115977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc5fce86e3a84ba35d6a9f9a976bd027569095ac890bb0a9be084a7b6d46a8e`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0e5434baa9330313b9e3fe8158f7e429b8e6f670f7827e3d0b7bf783db8f5`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c8b5d6672a8acbff82111478e566e99d328c19367e2426131038f2ad1101b6`  
		Last Modified: Tue, 17 Sep 2024 04:22:22 GMT  
		Size: 282.7 MB (282658342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4717836e6ba984fc7e2a5e5e86a7e251416b3dccb6040be18f200469fec02a`  
		Last Modified: Tue, 17 Sep 2024 04:22:07 GMT  
		Size: 4.3 KB (4269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569999b58754be6473e229c5114aa00e6999a4907396b2a2e44dc2fc063ce193`  
		Last Modified: Tue, 17 Sep 2024 04:22:07 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0bc18663cead1ed7c1bbf9052fa48a88bb214803211bbd482a1377a842a269`  
		Last Modified: Tue, 17 Sep 2024 04:22:07 GMT  
		Size: 10.9 KB (10875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64380beeb5f251b54bee028039ca0eb691da3f520e39ccf707dd77f4b4a18907`  
		Last Modified: Tue, 17 Sep 2024 04:22:08 GMT  
		Size: 1.6 MB (1595530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6` - unknown; unknown

```console
$ docker pull solr@sha256:ceef404d0c62010caeb98e7b7e37aa8f45674c10b53421c74cd2dbe85d37d164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4168009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a6f5083dc7a9dd73d046412b1e6ac3dff2eb45d3953225b6268ad344b5a6f6`

```dockerfile
```

-	Layers:
	-	`sha256:3e7ed63d3793472b1a2fabdd1f806658700691a9418bd45fff1d2946d1316bcf`  
		Last Modified: Tue, 17 Sep 2024 04:22:08 GMT  
		Size: 4.1 MB (4134507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bea49571cf576f2198cdcbf42d99b55ec12a8ce2401407f12b443f386636ce4`  
		Last Modified: Tue, 17 Sep 2024 04:22:07 GMT  
		Size: 33.5 KB (33502 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.6` - linux; s390x

```console
$ docker pull solr@sha256:a34b93c7c5a3b618ffd7e088cc20afff86a9acbe1dea126b6c065d8a09def032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.7 MB (369669547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f14962b54226abd423a127c375c146607d959e7305bab60e5bcee26b70eaee`
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
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64fbd7aebae0b0a6747cdd55eca436e86c96aadfe956fd593da55d6354278f6`  
		Last Modified: Tue, 17 Sep 2024 03:52:10 GMT  
		Size: 282.7 MB (282658019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4cbe8cd5936585c0bbae57ae1725e7a15b0f79e36e57167c1f917f96839ed0`  
		Last Modified: Tue, 17 Sep 2024 03:52:06 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f86c781663bbe7e459955338f80cf6eae6a4505f44dc11db7b6ce55b900ce7`  
		Last Modified: Tue, 17 Sep 2024 03:52:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635b98402103cceabb3eb6efde08fc91c9eeed0ace793dccb2dad7855e1ef02f`  
		Last Modified: Tue, 17 Sep 2024 03:52:06 GMT  
		Size: 10.9 KB (10874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089de77e2a50a61da9344feef37fbbfe55dfb32ef07137a56d13d9bfd49f813c`  
		Last Modified: Tue, 17 Sep 2024 03:52:07 GMT  
		Size: 1.5 MB (1535213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6` - unknown; unknown

```console
$ docker pull solr@sha256:7e9a0e905ecf7409704a882d1620c2678a896b45b40ddcec1e87ae192f89eda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4164583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e84135d11f9b21de254b86820e2192f83cb7b8e094e1ed1bf817773b4a25f52`

```dockerfile
```

-	Layers:
	-	`sha256:85576472d335ada074ca4471920bb9b097491b308f23754d9bc880802981ad38`  
		Last Modified: Tue, 17 Sep 2024 03:52:06 GMT  
		Size: 4.1 MB (4131114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53a8411dfe90c070d5bd530d91e7bb47010c6848322b5c8e6b04fd232280436f`  
		Last Modified: Tue, 17 Sep 2024 03:52:06 GMT  
		Size: 33.5 KB (33469 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.6-slim`

```console
$ docker pull solr@sha256:2242b630711a4d4ac40443053c21036c0d5f788168e27619e96006f549147387
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

### `solr:9.6-slim` - linux; amd64

```console
$ docker pull solr@sha256:fb80fa43635718e5468ffc65a79b0f7cd505f52fc31d7f8764b294b8f8b69578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156913455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaf82c87c6958c5db108a11dcbaad5251fceaf426a7dee753b4165cc1032f72`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efa5b12754637dd28292d2f806d9ed111c778e62292e749539fcc3e31c8bf88`  
		Last Modified: Tue, 17 Sep 2024 01:59:53 GMT  
		Size: 64.7 MB (64716314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3652726576b5dd7625a6fe4313b324b2114300648299485a06c7b164d673b4`  
		Last Modified: Tue, 17 Sep 2024 01:59:52 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b471aa85ebd460fadd7a1e7fc61ed38ecbde51082735a31090777f2309d345a3`  
		Last Modified: Tue, 17 Sep 2024 01:59:52 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b72f925600bd807e32092d1f489a56c6e69b06bcb91aabbabbe5bb1b7faa8e`  
		Last Modified: Tue, 17 Sep 2024 01:59:52 GMT  
		Size: 10.8 KB (10782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acccfbd619b0377ce36ab1b37248ba72180e3ba22e9d02311c73766daa883c63`  
		Last Modified: Tue, 17 Sep 2024 01:59:53 GMT  
		Size: 1.6 MB (1588577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6-slim` - unknown; unknown

```console
$ docker pull solr@sha256:8885b2e4e01473d1f41923fde2d3699a6f5eec5e8427a8cd2228fe9d315240f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 KB (35169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567761ab439888589f1b3b4e0aaf9017204160563d7c949bcd9e629cbe012d10`

```dockerfile
```

-	Layers:
	-	`sha256:25232f87036f4c1d6a59c6ce7e340c18f35ecba84f778a85e3b1db0ecdf8587c`  
		Last Modified: Tue, 17 Sep 2024 01:59:52 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4853d82e68f0709c56f1ce7ce6dda2b6310b09ca1f18cf2b101be03e0aef7555`  
		Last Modified: Tue, 17 Sep 2024 01:59:52 GMT  
		Size: 33.5 KB (33526 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.6-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:55714158626a01a40f6e91cd1922274c179d3d721439b0cf0242e087aa73658e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154138042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b425627131eb0ee81fe175b7c1652ceb2a493b604bca077a7b6c8f544e5d2c`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abadc6a78b245cdfdd8dc814d3cef3a3e3784ad15f7586db4649baaedcd54c7f`  
		Last Modified: Tue, 17 Sep 2024 06:22:52 GMT  
		Size: 64.7 MB (64716429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a610b31cf60cd2e0b10994c8c747b5a026b1b1861712f8817f73842f25201579`  
		Last Modified: Tue, 17 Sep 2024 06:22:50 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aefd5b93bcb00c5e977b335d726cfc0c7995a2bded0932fb873e7dcfb03bb62`  
		Last Modified: Tue, 17 Sep 2024 06:22:50 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dd832b53fdd4aab0422a3fa52f7e7fa0dc37873ce45c91125aa4ab9d8fefde`  
		Last Modified: Tue, 17 Sep 2024 06:22:50 GMT  
		Size: 10.8 KB (10782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf21e69534f04897cced22500ce7fa42f9cc371e41b5822c2a775c7a95b73c6`  
		Last Modified: Tue, 17 Sep 2024 06:22:51 GMT  
		Size: 1.4 MB (1447400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6-slim` - unknown; unknown

```console
$ docker pull solr@sha256:95dec7a390a251987edf978732cb7f269374a0cde3a17f129ab9be1f9c2d5426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c404adc6e5129cca611d3eed8b5954aee14f5fd5b87cac0d8e849cf16402317e`

```dockerfile
```

-	Layers:
	-	`sha256:c4cd93f1d11641648578c051893928fbdbe58854a2d672eeb8f4951c81aa4f85`  
		Last Modified: Tue, 17 Sep 2024 06:22:50 GMT  
		Size: 3.7 MB (3703862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:665f953737a84acd61361e2afeb9274ef60959ab314d8441c2abd8e4ecddc9a3`  
		Last Modified: Tue, 17 Sep 2024 06:22:50 GMT  
		Size: 33.8 KB (33819 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.6-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:fca5408e27b6b422a66bc205091d82f7f070724e163886a568290d1677afeb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162746257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c572b08cd462c931127cffc3d1c6cf7e73ab52e0ca4567bbc06d40c0505bb0c3`
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
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
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
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2709165c356fd5bb9b4cda23232d8784bb71b95b05f605dc769df016474e33`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.1 MB (47115977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc5fce86e3a84ba35d6a9f9a976bd027569095ac890bb0a9be084a7b6d46a8e`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0e5434baa9330313b9e3fe8158f7e429b8e6f670f7827e3d0b7bf783db8f5`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edff8ea831f57a46a44c78545f564beb821ff5d3533ce516934ac2daedb43b7a`  
		Last Modified: Tue, 17 Sep 2024 04:23:37 GMT  
		Size: 64.7 MB (64716770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc3e02f902b7509030c79dd2dee191df69d774f7a20411a211aefaf605c434b`  
		Last Modified: Tue, 17 Sep 2024 04:23:35 GMT  
		Size: 4.3 KB (4271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713c0ddda084ccabe9f225d12e4f87a7840b76c69abf0a94b1d26ce43606f946`  
		Last Modified: Tue, 17 Sep 2024 04:23:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab332d4b637f4fe224ed160103849cee9bb7d7bb5980eba9338359c43f43b4e`  
		Last Modified: Tue, 17 Sep 2024 04:23:35 GMT  
		Size: 10.8 KB (10786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88c970d5cd99fbaac5d9bf9c4ac850a7ba69e7ea412ebf3da424d1f57759b64`  
		Last Modified: Tue, 17 Sep 2024 04:23:36 GMT  
		Size: 1.6 MB (1595516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6-slim` - unknown; unknown

```console
$ docker pull solr@sha256:62762f78d20eab7278b939995d6307fa7ae8f0fce475568cfa80d6075b4b43bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e12d7c29680fcaf27bf180bbf80c8e5b4549daae5a74994ea432bac11881a4d`

```dockerfile
```

-	Layers:
	-	`sha256:f5f35230471800653fb784b4618fddd50bbd27639430f7b577e766446f1a5eea`  
		Last Modified: Tue, 17 Sep 2024 04:23:35 GMT  
		Size: 3.7 MB (3708107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a197b8ca67cea8933e34c37aacd3a79cf9db45dcd662f035e0a102f1751a45c`  
		Last Modified: Tue, 17 Sep 2024 04:23:35 GMT  
		Size: 33.6 KB (33559 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.6-slim` - linux; s390x

```console
$ docker pull solr@sha256:7847adca1234ed0ad0c035c86647e424600fe0bc179515ca015b64bfab9f0bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151727982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084e1e971334ae82e62e026631b82970fd8fed7f73b3dc3761ea802779351ea2`
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
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
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
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438dd0f9f109d012ce40e372fde83bac7871ab764c2b9102181753fdd10c6955`  
		Last Modified: Tue, 17 Sep 2024 03:53:07 GMT  
		Size: 64.7 MB (64716483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9942a04e7be11cc37e0c2c9fafb2c2df9213033f8ce703ed285716a129d9de2`  
		Last Modified: Tue, 17 Sep 2024 03:53:05 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f18f69d48c13411ca869c0019c6c2eb6c96e8cbac0908870f302c9fd44978ac`  
		Last Modified: Tue, 17 Sep 2024 03:53:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b1ba3c667f10dca84369499deff98d7c6aa7ca3a46af799ad1f46aa25504ce`  
		Last Modified: Tue, 17 Sep 2024 03:53:05 GMT  
		Size: 10.8 KB (10783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f140c95b540f042e86bdee3c0e682115855cdad4544b798025848e9d135e6b1e`  
		Last Modified: Tue, 17 Sep 2024 03:53:06 GMT  
		Size: 1.5 MB (1535272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6-slim` - unknown; unknown

```console
$ docker pull solr@sha256:700bda47929bf73bb92279f4dcc7e189522fa9ef2003d8b8b275beeb77160eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ab08fb706d76bfb990f0b43ec947372e40241fe253d8ee8ddc30303480b1e3`

```dockerfile
```

-	Layers:
	-	`sha256:8002b63cb2103605f1a0f203c7270f2032463dafd3bc54d7cc9d9d5ab9ec1ae8`  
		Last Modified: Tue, 17 Sep 2024 03:53:06 GMT  
		Size: 3.7 MB (3704714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29dcd4d8b9c149e34edf3819e6f69236a78d4c603f9cda0ac56b964c1d8bd025`  
		Last Modified: Tue, 17 Sep 2024 03:53:05 GMT  
		Size: 33.5 KB (33525 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.6.1`

```console
$ docker pull solr@sha256:21aa3ccfc2dcd1365dd84e23798c8755f16d936e42d767f7ba65c298ef14891d
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

### `solr:9.6.1` - linux; amd64

```console
$ docker pull solr@sha256:eb81e5e1aa2b0a24cdfce10002e04738c15e5493b34ea61d8ffbfa5e145ecff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.9 MB (374854880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5606750d95b24167dd5a2300936a4efd18655a050726dd6b745bc712b0b19840`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee6ff2cba794811e53bd23f5d7e7f4b587421632b8e25ca1e65c97ae1003e41`  
		Last Modified: Tue, 17 Sep 2024 02:00:51 GMT  
		Size: 282.7 MB (282657709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b4af993082e9b9234927f53528aed82fdb52b4682dc15d91a5d0289ddc57d`  
		Last Modified: Tue, 17 Sep 2024 02:00:44 GMT  
		Size: 4.3 KB (4269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfc8d8a4b67f139a87f9dd28c07e1ef53024776af8f665a5bf4d7d47c354710`  
		Last Modified: Tue, 17 Sep 2024 02:00:44 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433f5b970a160ef67e0ec69d75118b99ee9233a7e4292b088fba071ec0c8a32b`  
		Last Modified: Tue, 17 Sep 2024 02:00:44 GMT  
		Size: 10.9 KB (10870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025719eb0bae9901858e2be995667919d14c7075f6cee07b8424d72344b37f1a`  
		Last Modified: Tue, 17 Sep 2024 02:00:46 GMT  
		Size: 1.6 MB (1588525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6.1` - unknown; unknown

```console
$ docker pull solr@sha256:aa7ed4bad7856d7853ae4d8cdc89394be4b5c22dc3d7f8f02b4dbbdd9128b21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4163462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e6be1fcf1c318e73a5808c280041e5798c86d2b417ae5d04ea1dce8d6e1507`

```dockerfile
```

-	Layers:
	-	`sha256:74f32183e5315da7b171e393eae2a693ac19fb1b7aa53b91f91bb682e3d5ac09`  
		Last Modified: Tue, 17 Sep 2024 02:00:45 GMT  
		Size: 4.1 MB (4129993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2385ae3be093cb067dd65dd88fce7a35909d83243eb6013db4fb903ef4c05baf`  
		Last Modified: Tue, 17 Sep 2024 02:00:44 GMT  
		Size: 33.5 KB (33469 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.6.1` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:e70271df54957f08f0bbcc8262b35bde86652dcc2799aa5479f3147f49668bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.1 MB (372079616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba793ebde9e3034a55209bc053a019ef3b007b3facaa57253d3184b804db1262`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed8e54022b4dd9c5d0c209217dcf58d4b3a44b51e0e5dbd6fef3750de645adc`  
		Last Modified: Tue, 17 Sep 2024 06:22:08 GMT  
		Size: 282.7 MB (282657893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ef56b6938a107d06eba1cb1f1af513128b0aaaee112de6adaab995cb8d519f`  
		Last Modified: Tue, 17 Sep 2024 06:22:00 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2848e3662dfcd73d5567bf2154dbb89db8c8497e4646ff0d8ef61d9862c607e8`  
		Last Modified: Tue, 17 Sep 2024 06:22:00 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c269f24ca86ff9ce654e5060a73c56225782c2ac869261f5651aa2083b0860`  
		Last Modified: Tue, 17 Sep 2024 06:22:00 GMT  
		Size: 10.9 KB (10868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69814293d747ca42cd11b1080b8ee13e7cfb653e8f24030b24e88dd20987166c`  
		Last Modified: Tue, 17 Sep 2024 06:22:01 GMT  
		Size: 1.4 MB (1447424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6.1` - unknown; unknown

```console
$ docker pull solr@sha256:17da78638eef92203746cd654e1fc9a7dc6388cd89a7a14c89617ed725b78cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4164024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310f7530e445b1015ed07e82ae070fd74469c79c4f20d25d235904b52b56ae85`

```dockerfile
```

-	Layers:
	-	`sha256:a8a987b553496f672fe6bd20eb7bcd6411a8156a94b93870098c9c8fee599b7f`  
		Last Modified: Tue, 17 Sep 2024 06:22:00 GMT  
		Size: 4.1 MB (4130262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f19f59ab6c50b79aaab071bebd06fcb8901351e93dd95dab171ebc3c2bbae583`  
		Last Modified: Tue, 17 Sep 2024 06:21:59 GMT  
		Size: 33.8 KB (33762 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.6.1` - linux; ppc64le

```console
$ docker pull solr@sha256:12c3311761e780d32afcfadc82231bd36fc84155ba2b9eee980fa2ee00fe182f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380687925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457e05e485b18d9edbe78b48c2a5e26c74bc3bbf69fc874c777bf6ced25c9696`
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
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2709165c356fd5bb9b4cda23232d8784bb71b95b05f605dc769df016474e33`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.1 MB (47115977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc5fce86e3a84ba35d6a9f9a976bd027569095ac890bb0a9be084a7b6d46a8e`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0e5434baa9330313b9e3fe8158f7e429b8e6f670f7827e3d0b7bf783db8f5`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c8b5d6672a8acbff82111478e566e99d328c19367e2426131038f2ad1101b6`  
		Last Modified: Tue, 17 Sep 2024 04:22:22 GMT  
		Size: 282.7 MB (282658342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4717836e6ba984fc7e2a5e5e86a7e251416b3dccb6040be18f200469fec02a`  
		Last Modified: Tue, 17 Sep 2024 04:22:07 GMT  
		Size: 4.3 KB (4269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569999b58754be6473e229c5114aa00e6999a4907396b2a2e44dc2fc063ce193`  
		Last Modified: Tue, 17 Sep 2024 04:22:07 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0bc18663cead1ed7c1bbf9052fa48a88bb214803211bbd482a1377a842a269`  
		Last Modified: Tue, 17 Sep 2024 04:22:07 GMT  
		Size: 10.9 KB (10875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64380beeb5f251b54bee028039ca0eb691da3f520e39ccf707dd77f4b4a18907`  
		Last Modified: Tue, 17 Sep 2024 04:22:08 GMT  
		Size: 1.6 MB (1595530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6.1` - unknown; unknown

```console
$ docker pull solr@sha256:ceef404d0c62010caeb98e7b7e37aa8f45674c10b53421c74cd2dbe85d37d164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4168009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a6f5083dc7a9dd73d046412b1e6ac3dff2eb45d3953225b6268ad344b5a6f6`

```dockerfile
```

-	Layers:
	-	`sha256:3e7ed63d3793472b1a2fabdd1f806658700691a9418bd45fff1d2946d1316bcf`  
		Last Modified: Tue, 17 Sep 2024 04:22:08 GMT  
		Size: 4.1 MB (4134507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bea49571cf576f2198cdcbf42d99b55ec12a8ce2401407f12b443f386636ce4`  
		Last Modified: Tue, 17 Sep 2024 04:22:07 GMT  
		Size: 33.5 KB (33502 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.6.1` - linux; s390x

```console
$ docker pull solr@sha256:a34b93c7c5a3b618ffd7e088cc20afff86a9acbe1dea126b6c065d8a09def032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.7 MB (369669547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f14962b54226abd423a127c375c146607d959e7305bab60e5bcee26b70eaee`
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
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_VERSION=9.6.1
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DIST=
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Wed, 29 May 2024 20:45:28 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
# ARGS: SOLR_VERSION=9.6.1 SOLR_DIST= SOLR_SHA512=7e16aa71fc01f9d9b05e5514e35798104a18253a211426aa669aa3b91225d110a4fa1c78c9ec86b7e1909e2aae63696deffd877536790303cd0638eb7f1a8c63 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
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
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64fbd7aebae0b0a6747cdd55eca436e86c96aadfe956fd593da55d6354278f6`  
		Last Modified: Tue, 17 Sep 2024 03:52:10 GMT  
		Size: 282.7 MB (282658019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4cbe8cd5936585c0bbae57ae1725e7a15b0f79e36e57167c1f917f96839ed0`  
		Last Modified: Tue, 17 Sep 2024 03:52:06 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f86c781663bbe7e459955338f80cf6eae6a4505f44dc11db7b6ce55b900ce7`  
		Last Modified: Tue, 17 Sep 2024 03:52:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635b98402103cceabb3eb6efde08fc91c9eeed0ace793dccb2dad7855e1ef02f`  
		Last Modified: Tue, 17 Sep 2024 03:52:06 GMT  
		Size: 10.9 KB (10874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089de77e2a50a61da9344feef37fbbfe55dfb32ef07137a56d13d9bfd49f813c`  
		Last Modified: Tue, 17 Sep 2024 03:52:07 GMT  
		Size: 1.5 MB (1535213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6.1` - unknown; unknown

```console
$ docker pull solr@sha256:7e9a0e905ecf7409704a882d1620c2678a896b45b40ddcec1e87ae192f89eda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4164583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e84135d11f9b21de254b86820e2192f83cb7b8e094e1ed1bf817773b4a25f52`

```dockerfile
```

-	Layers:
	-	`sha256:85576472d335ada074ca4471920bb9b097491b308f23754d9bc880802981ad38`  
		Last Modified: Tue, 17 Sep 2024 03:52:06 GMT  
		Size: 4.1 MB (4131114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53a8411dfe90c070d5bd530d91e7bb47010c6848322b5c8e6b04fd232280436f`  
		Last Modified: Tue, 17 Sep 2024 03:52:06 GMT  
		Size: 33.5 KB (33469 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.6.1-slim`

```console
$ docker pull solr@sha256:2242b630711a4d4ac40443053c21036c0d5f788168e27619e96006f549147387
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

### `solr:9.6.1-slim` - linux; amd64

```console
$ docker pull solr@sha256:fb80fa43635718e5468ffc65a79b0f7cd505f52fc31d7f8764b294b8f8b69578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156913455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaf82c87c6958c5db108a11dcbaad5251fceaf426a7dee753b4165cc1032f72`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efa5b12754637dd28292d2f806d9ed111c778e62292e749539fcc3e31c8bf88`  
		Last Modified: Tue, 17 Sep 2024 01:59:53 GMT  
		Size: 64.7 MB (64716314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3652726576b5dd7625a6fe4313b324b2114300648299485a06c7b164d673b4`  
		Last Modified: Tue, 17 Sep 2024 01:59:52 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b471aa85ebd460fadd7a1e7fc61ed38ecbde51082735a31090777f2309d345a3`  
		Last Modified: Tue, 17 Sep 2024 01:59:52 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b72f925600bd807e32092d1f489a56c6e69b06bcb91aabbabbe5bb1b7faa8e`  
		Last Modified: Tue, 17 Sep 2024 01:59:52 GMT  
		Size: 10.8 KB (10782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acccfbd619b0377ce36ab1b37248ba72180e3ba22e9d02311c73766daa883c63`  
		Last Modified: Tue, 17 Sep 2024 01:59:53 GMT  
		Size: 1.6 MB (1588577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6.1-slim` - unknown; unknown

```console
$ docker pull solr@sha256:8885b2e4e01473d1f41923fde2d3699a6f5eec5e8427a8cd2228fe9d315240f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 KB (35169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567761ab439888589f1b3b4e0aaf9017204160563d7c949bcd9e629cbe012d10`

```dockerfile
```

-	Layers:
	-	`sha256:25232f87036f4c1d6a59c6ce7e340c18f35ecba84f778a85e3b1db0ecdf8587c`  
		Last Modified: Tue, 17 Sep 2024 01:59:52 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4853d82e68f0709c56f1ce7ce6dda2b6310b09ca1f18cf2b101be03e0aef7555`  
		Last Modified: Tue, 17 Sep 2024 01:59:52 GMT  
		Size: 33.5 KB (33526 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.6.1-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:55714158626a01a40f6e91cd1922274c179d3d721439b0cf0242e087aa73658e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154138042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b425627131eb0ee81fe175b7c1652ceb2a493b604bca077a7b6c8f544e5d2c`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abadc6a78b245cdfdd8dc814d3cef3a3e3784ad15f7586db4649baaedcd54c7f`  
		Last Modified: Tue, 17 Sep 2024 06:22:52 GMT  
		Size: 64.7 MB (64716429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a610b31cf60cd2e0b10994c8c747b5a026b1b1861712f8817f73842f25201579`  
		Last Modified: Tue, 17 Sep 2024 06:22:50 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aefd5b93bcb00c5e977b335d726cfc0c7995a2bded0932fb873e7dcfb03bb62`  
		Last Modified: Tue, 17 Sep 2024 06:22:50 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dd832b53fdd4aab0422a3fa52f7e7fa0dc37873ce45c91125aa4ab9d8fefde`  
		Last Modified: Tue, 17 Sep 2024 06:22:50 GMT  
		Size: 10.8 KB (10782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf21e69534f04897cced22500ce7fa42f9cc371e41b5822c2a775c7a95b73c6`  
		Last Modified: Tue, 17 Sep 2024 06:22:51 GMT  
		Size: 1.4 MB (1447400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6.1-slim` - unknown; unknown

```console
$ docker pull solr@sha256:95dec7a390a251987edf978732cb7f269374a0cde3a17f129ab9be1f9c2d5426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c404adc6e5129cca611d3eed8b5954aee14f5fd5b87cac0d8e849cf16402317e`

```dockerfile
```

-	Layers:
	-	`sha256:c4cd93f1d11641648578c051893928fbdbe58854a2d672eeb8f4951c81aa4f85`  
		Last Modified: Tue, 17 Sep 2024 06:22:50 GMT  
		Size: 3.7 MB (3703862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:665f953737a84acd61361e2afeb9274ef60959ab314d8441c2abd8e4ecddc9a3`  
		Last Modified: Tue, 17 Sep 2024 06:22:50 GMT  
		Size: 33.8 KB (33819 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.6.1-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:fca5408e27b6b422a66bc205091d82f7f070724e163886a568290d1677afeb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162746257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c572b08cd462c931127cffc3d1c6cf7e73ab52e0ca4567bbc06d40c0505bb0c3`
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
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
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
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2709165c356fd5bb9b4cda23232d8784bb71b95b05f605dc769df016474e33`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.1 MB (47115977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc5fce86e3a84ba35d6a9f9a976bd027569095ac890bb0a9be084a7b6d46a8e`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0e5434baa9330313b9e3fe8158f7e429b8e6f670f7827e3d0b7bf783db8f5`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edff8ea831f57a46a44c78545f564beb821ff5d3533ce516934ac2daedb43b7a`  
		Last Modified: Tue, 17 Sep 2024 04:23:37 GMT  
		Size: 64.7 MB (64716770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc3e02f902b7509030c79dd2dee191df69d774f7a20411a211aefaf605c434b`  
		Last Modified: Tue, 17 Sep 2024 04:23:35 GMT  
		Size: 4.3 KB (4271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713c0ddda084ccabe9f225d12e4f87a7840b76c69abf0a94b1d26ce43606f946`  
		Last Modified: Tue, 17 Sep 2024 04:23:35 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab332d4b637f4fe224ed160103849cee9bb7d7bb5980eba9338359c43f43b4e`  
		Last Modified: Tue, 17 Sep 2024 04:23:35 GMT  
		Size: 10.8 KB (10786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88c970d5cd99fbaac5d9bf9c4ac850a7ba69e7ea412ebf3da424d1f57759b64`  
		Last Modified: Tue, 17 Sep 2024 04:23:36 GMT  
		Size: 1.6 MB (1595516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6.1-slim` - unknown; unknown

```console
$ docker pull solr@sha256:62762f78d20eab7278b939995d6307fa7ae8f0fce475568cfa80d6075b4b43bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e12d7c29680fcaf27bf180bbf80c8e5b4549daae5a74994ea432bac11881a4d`

```dockerfile
```

-	Layers:
	-	`sha256:f5f35230471800653fb784b4618fddd50bbd27639430f7b577e766446f1a5eea`  
		Last Modified: Tue, 17 Sep 2024 04:23:35 GMT  
		Size: 3.7 MB (3708107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a197b8ca67cea8933e34c37aacd3a79cf9db45dcd662f035e0a102f1751a45c`  
		Last Modified: Tue, 17 Sep 2024 04:23:35 GMT  
		Size: 33.6 KB (33559 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.6.1-slim` - linux; s390x

```console
$ docker pull solr@sha256:7847adca1234ed0ad0c035c86647e424600fe0bc179515ca015b64bfab9f0bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151727982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084e1e971334ae82e62e026631b82970fd8fed7f73b3dc3761ea802779351ea2`
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
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 29 May 2024 20:45:28 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 May 2024 20:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 20:45:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:45:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 29 May 2024 20:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 May 2024 20:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 May 2024 20:45:28 GMT
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
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438dd0f9f109d012ce40e372fde83bac7871ab764c2b9102181753fdd10c6955`  
		Last Modified: Tue, 17 Sep 2024 03:53:07 GMT  
		Size: 64.7 MB (64716483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9942a04e7be11cc37e0c2c9fafb2c2df9213033f8ce703ed285716a129d9de2`  
		Last Modified: Tue, 17 Sep 2024 03:53:05 GMT  
		Size: 4.3 KB (4305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f18f69d48c13411ca869c0019c6c2eb6c96e8cbac0908870f302c9fd44978ac`  
		Last Modified: Tue, 17 Sep 2024 03:53:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b1ba3c667f10dca84369499deff98d7c6aa7ca3a46af799ad1f46aa25504ce`  
		Last Modified: Tue, 17 Sep 2024 03:53:05 GMT  
		Size: 10.8 KB (10783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f140c95b540f042e86bdee3c0e682115855cdad4544b798025848e9d135e6b1e`  
		Last Modified: Tue, 17 Sep 2024 03:53:06 GMT  
		Size: 1.5 MB (1535272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.6.1-slim` - unknown; unknown

```console
$ docker pull solr@sha256:700bda47929bf73bb92279f4dcc7e189522fa9ef2003d8b8b275beeb77160eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ab08fb706d76bfb990f0b43ec947372e40241fe253d8ee8ddc30303480b1e3`

```dockerfile
```

-	Layers:
	-	`sha256:8002b63cb2103605f1a0f203c7270f2032463dafd3bc54d7cc9d9d5ab9ec1ae8`  
		Last Modified: Tue, 17 Sep 2024 03:53:06 GMT  
		Size: 3.7 MB (3704714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29dcd4d8b9c149e34edf3819e6f69236a78d4c603f9cda0ac56b964c1d8bd025`  
		Last Modified: Tue, 17 Sep 2024 03:53:05 GMT  
		Size: 33.5 KB (33525 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.7`

```console
$ docker pull solr@sha256:4267344d8d37c5982894f8424e923a66e21461fc2d61602d935837d5d464182b
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
$ docker pull solr@sha256:c56b658c959f8ad2b7389d9b0107b48e3f95f13419788300f1f1297f198abdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.3 MB (375281077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d0bd9e56bc994ea086b4d7169937de4f8db32e98b1d481b13ec19856ebf830`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1aa583d1ef98fcaf42e21c147c70dd631fa34b36dc593c64265c54921dfd03`  
		Last Modified: Tue, 17 Sep 2024 01:58:19 GMT  
		Size: 283.1 MB (283083900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350cf53fd52a58d48f5d69688ffa4f77f51394ce81c3e6e81cb986dc1bba540d`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 4.3 KB (4270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b317c36e5a1025abf32228209e48b34ad153043e1bf9998c560e0b6e4e727164`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf7dd409191fcd1d9d51f54e8bfabeb0a53eca08b8da688a07588992f36b52c`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 10.9 KB (10867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24483e359719eee7ece7e8523546cd960c86efecf9b6990a080cbfdeb511ed1`  
		Last Modified: Tue, 17 Sep 2024 01:58:16 GMT  
		Size: 1.6 MB (1588536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7` - unknown; unknown

```console
$ docker pull solr@sha256:116ea6808bd356110ff347fb2574c286b721260a361f2e4ce35c6c678805e065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf593f0ad90c7de914051d98bb6b2ddf483c741f512f5d6842d0cc84b6e2af44`

```dockerfile
```

-	Layers:
	-	`sha256:77ffd5df8f3b12549b2e1216fd01df2f73b62374c87491ce014674f558833868`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 4.2 MB (4150903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c21b111477b68635e4f4ae71603feb8b8130a7feb123ba9b0d691d17b3ee7c55`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 34.0 KB (34047 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:4ceca4ac998615dc3a80f7e67cf92dbd847e8e0bc04237f6f9f2928e75e82882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.5 MB (372505844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1026faf3194f8160c949410787ea9ffedf89e75772f25ecded9856195b0628e3`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257dbd9b6c377e0e75f4fe02716f6f373ee72cb589786a680f1100c695eaeb7a`  
		Last Modified: Tue, 17 Sep 2024 06:19:49 GMT  
		Size: 283.1 MB (283084078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f21f0a74e3bbc74b2541e017928f67aa6d3a04761bcf33faea7de058243d2c`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c12824d064498f7b2618f5c761d37409e87c6988cbc3b467b4c7f97e11fc5a1`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3aecd7313dcf51494ca18f98fb241d436e70d7b029239ba20b93d3d3d489b6`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 10.9 KB (10866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779e44c15834a5a622a574b87658e1eea3fe44616ee17308d5913942c21143fb`  
		Last Modified: Tue, 17 Sep 2024 06:19:45 GMT  
		Size: 1.4 MB (1447466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7` - unknown; unknown

```console
$ docker pull solr@sha256:e0a29761c26bec3ef130ef5c7d2d315ce715b0d10adaf2d1b1f01bd83b8c323a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4185560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d057f70f18b40b0e4d653edffbca453948a50642e3b3b73f3152c6e4785a342f`

```dockerfile
```

-	Layers:
	-	`sha256:0212511128601e44c88cca991fabc909ad9628577f68ee3d509facdb93f12d04`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 4.2 MB (4151196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b27012cb6170b8ae603f9c2a10a700f3e3b886e6ffcc9626104a9fb3fdb6481`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 34.4 KB (34364 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7` - linux; ppc64le

```console
$ docker pull solr@sha256:8b600bef8663026dc5874367d43a9c3b59236b3c75318ce6373ee4a2c20136eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381114029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09b1467a0770309e9acfdcac3b31cde50317cb57fb054cafc3e84e743017018`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2709165c356fd5bb9b4cda23232d8784bb71b95b05f605dc769df016474e33`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.1 MB (47115977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc5fce86e3a84ba35d6a9f9a976bd027569095ac890bb0a9be084a7b6d46a8e`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0e5434baa9330313b9e3fe8158f7e429b8e6f670f7827e3d0b7bf783db8f5`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9166f7814dcdbd5edcd0d198132f7d73400d07b553026275a8342b616828d4`  
		Last Modified: Tue, 17 Sep 2024 04:18:51 GMT  
		Size: 283.1 MB (283084447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fa47877401d2d997531c42aef453f1eedc981d83852613e4ffca8477d4dfc8`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 4.3 KB (4272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d41a688a4887ac1150669945f16640ce2f3ac7cf475e467466c3ef6a1c93388`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c4bd764cd9f26217ca67a27b61282e8017b5aacf46c492a07431fecbd6a45e`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 10.9 KB (10869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e3bd936391e4c95488f614d045b4a5051908e7a29245e0843e46cb0bbac3ba`  
		Last Modified: Tue, 17 Sep 2024 04:18:37 GMT  
		Size: 1.6 MB (1595531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7` - unknown; unknown

```console
$ docker pull solr@sha256:59588f3a8c982f85ce93be7a1d83ee2ecdc7d792b86d2e0eeff44ad435bdd32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953461ab2f2864fe202fd7a6d9870b694ab1e34170ea32e106993b64fe26425f`

```dockerfile
```

-	Layers:
	-	`sha256:6c494bbe8b57e7dd6714c1808135ff95ab2809e144769c06eddedf7bebae47ba`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 4.2 MB (4155429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e059d40138e1cee3c2b194f47ce62337b83272ba72e5d47b87ab59fbcf2f1e7a`  
		Last Modified: Tue, 17 Sep 2024 04:18:35 GMT  
		Size: 34.1 KB (34093 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7` - linux; s390x

```console
$ docker pull solr@sha256:0bd26f3815d4fbefdbc761da39c01cd601d74ee2b09555e49dc96d107fcbe1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370095765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3da1f9242c39468fe09d3e3fc38d13b71ff16f3bb82a6267fc404c9384f1c85`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd33900eddbaad7aef6f3b868400a94709edd5e4d439c0e7bf926ca7c34f184`  
		Last Modified: Tue, 17 Sep 2024 03:49:44 GMT  
		Size: 283.1 MB (283084224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d394f36e696d6e8145c7a7e05e50accc945e8347475575e3f8f3689b66646c8`  
		Last Modified: Tue, 17 Sep 2024 03:49:38 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b9a8d32862a02e8f90876527c50eea0d08b003a77bc1ed996341d57c4a206b`  
		Last Modified: Tue, 17 Sep 2024 03:49:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338736aa5b5c8d8c26d0208cd61c557a4ff9296d102001a445c72e802fcf10b6`  
		Last Modified: Tue, 17 Sep 2024 03:49:39 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95b165658950bff630dcbbedda6c18c58b3f786eda04774cd52c499e8b450ef`  
		Last Modified: Tue, 17 Sep 2024 03:49:40 GMT  
		Size: 1.5 MB (1535227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7` - unknown; unknown

```console
$ docker pull solr@sha256:077ce584ebc58a06dd0bfdd36085167a7b6e1c793ab986888f63446ca1cbd65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68118e13fe2e2840d191ff87b4cabfcf096b2764a3283fff584131964ae760c`

```dockerfile
```

-	Layers:
	-	`sha256:34f5f352acf6521c285cff397e1c9b7d735f1273e2a3d5e0455465e3a3974b1c`  
		Last Modified: Tue, 17 Sep 2024 03:49:39 GMT  
		Size: 4.2 MB (4152024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ecb0590de35c286840f10eeb7146a800dd09d72372f788ec9ea620e04b3319`  
		Last Modified: Tue, 17 Sep 2024 03:49:38 GMT  
		Size: 34.0 KB (34047 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.7-slim`

```console
$ docker pull solr@sha256:3191833409ac0349ebea8c9da9f2c8a0633ca67b184aeb1a36902e9b5d38539b
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
$ docker pull solr@sha256:5ff61de1418757425e028737bd010cb2a030b7a1955b8b9eea5de16a40f9ee9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157019263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb6986494c44f94ddfff0d1548a447d8fb79b7ecfa3559d8b2ccebc753753ea`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018cda53b3efa90b157c23cc92e3b69774f056abb446134fcbe3d15968857f5b`  
		Last Modified: Tue, 17 Sep 2024 01:58:08 GMT  
		Size: 64.8 MB (64822172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08103616a43c638c607be5d934ef046dc7bf8892966d0d961410f521e5a408f`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf3eabf6b02922222663f92fc056535dd5cd97dffb88684cfada2c309d3e9a5`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2fdc48848131a85389028e210f9f91b785eb6da8e2b928aebfa41cfab8261`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 10.8 KB (10782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec4a377ac5fd8f8ad2701146a5a77a47c863cc86c49c33b7028e3f178227759`  
		Last Modified: Tue, 17 Sep 2024 01:58:07 GMT  
		Size: 1.6 MB (1588526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7-slim` - unknown; unknown

```console
$ docker pull solr@sha256:7c01207568df7fdc13030f0e12715086f630e571609daa9f21c3bf1109809bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe29adbd3d3ea2cf6b3227d2161d33bcd0cfda642f758da5a8ba5db7b05bd00`

```dockerfile
```

-	Layers:
	-	`sha256:2220b180518a4ec4985d4aba0ce5f4709142a2e133ffe6c9f51724b30f086261`  
		Last Modified: Tue, 17 Sep 2024 01:58:06 GMT  
		Size: 3.7 MB (3706729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43757148e05e2334fb7b85597007c07bc672e833ed833c9be2de45452ca9f8db`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:195777fdbe8279808802bb4c2ff7b1041272f518a0f9159a332ff16d5a51f159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154244158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b542ab37706376e5ec336fe0a9b6b4caaaa37d4871b6e5056bd36db6068a3`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3acf7c85b7b1f4080586a56569199ed6f2666a97848ddf34af9b4e293115625`  
		Last Modified: Tue, 17 Sep 2024 06:20:40 GMT  
		Size: 64.8 MB (64822511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba76d9fa57a3a819707684b72833bd5aeefe6fc85ff3381d8e70dad81be1f757`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873080c20f3d3b7bdd26193c8dc28a1fd8e59f1bcbfdd76466cb23275c14d058`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630bf46d6ed4ff01c66668d72efe9a5a16e8687f695b1bc9d7b149102c059bfd`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 10.8 KB (10784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4d80fe3aa5c186c73106441598d6eb763e63207fbc6239f7dcb3a1224a3ce6`  
		Last Modified: Tue, 17 Sep 2024 06:20:40 GMT  
		Size: 1.4 MB (1447434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7-slim` - unknown; unknown

```console
$ docker pull solr@sha256:97407c4de63b8e01b224ee43dd35888e107b73681c837cfa38244c92b6658873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525e5ee236c9c5a45c300ce639ed98156bce968bdf4ca90be36f6fc7c6b5b414`

```dockerfile
```

-	Layers:
	-	`sha256:feee39d2f9c4621a59b06a62cfc026ac84f2fd59fe467da055d5a4896f295df3`  
		Last Modified: Tue, 17 Sep 2024 06:20:39 GMT  
		Size: 3.7 MB (3707022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f5788cdf11a8e7fc232a9a7e986fee1e36af56c55e911982d495c24dbdc12d`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:e474e41543c8a0f9d6c112656b3bc26c5ded6e7c7c877387fa247afe2dfdb728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162852273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cd1f1da329fdff8aa31f379d00d1a5f5f98a22361697b9188e7dcb7edc4641`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2709165c356fd5bb9b4cda23232d8784bb71b95b05f605dc769df016474e33`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.1 MB (47115977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc5fce86e3a84ba35d6a9f9a976bd027569095ac890bb0a9be084a7b6d46a8e`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0e5434baa9330313b9e3fe8158f7e429b8e6f670f7827e3d0b7bf783db8f5`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5cc63a136204177cb009444f1d4e30f778fa6342bc1fff3c415a2db26af859`  
		Last Modified: Tue, 17 Sep 2024 04:20:10 GMT  
		Size: 64.8 MB (64822807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f015af6089a3d3ce9ea59d066d6e2dfb91c3d75c469700392340d72a2cd9fb3`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 4.3 KB (4271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545d733fba4628b2bd6eac8273fb73a70b5ba52a64d8d929b83ecd8c6db0abba`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28954cd8d780db42f4455b9cd967947a7ccb6d8d238ae02092fa47cf80f3979f`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 10.8 KB (10787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c02cb793eafe46508fca732577230f3775f580de6283a3bef2bf557b2042a1`  
		Last Modified: Tue, 17 Sep 2024 04:20:09 GMT  
		Size: 1.6 MB (1595495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1e6d3fd4742692de1a98951978739b1424a65b1aacc6ae0274ee4c78aa185510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6632a300c80447bf453aa8a2d18ab3da903a6f2edd8f2fa73b4338503bab3d6`

```dockerfile
```

-	Layers:
	-	`sha256:466e5869a02f90160dd4ace6559b190ce24b3e1170f4b5245be5b7519f80dd99`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 3.7 MB (3711255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ec45fb6fec772aafb9e7bb001461fd296b07e2640a8da505888d788eaa2e4b`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 34.2 KB (34154 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7-slim` - linux; s390x

```console
$ docker pull solr@sha256:32aed8931be1df5fa8a4162fe06a48d6201aafb1ba297d28892987e501c8a5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151834055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a35a7e1018908896a4c1af9b4756ce7e9636fcb1561c19f630b9dd5a66a2c30`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2e4d148efe9b8ddc93fd95944cfa339847af273a2c1670177a272b9c577e49`  
		Last Modified: Tue, 17 Sep 2024 03:50:40 GMT  
		Size: 64.8 MB (64822613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de244efe4184c250f4ce53ad165d6e71af82b7a2d23601aefb5a7a5e2a08c098`  
		Last Modified: Tue, 17 Sep 2024 03:50:38 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75870b73c63df3e5916f4b20f3323eed537098164758505af69724e3eefe9b`  
		Last Modified: Tue, 17 Sep 2024 03:50:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dcf24f699c68c7dec74826b6f70798ec436579e1f7dd06eaaa1a8cf3cfe35a`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 10.8 KB (10784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319ac3aec22f66e31b317e2d05576e041647c7aa97cddc869c9a91a8366ef6d`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 1.5 MB (1535216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7-slim` - unknown; unknown

```console
$ docker pull solr@sha256:fac442f0523e1bb9886faace4e58d3b7cbc0683098f3de217f52c081df815a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b4502bc0be4c2e4b593a45180e288d60412f833f088ed4d31945adf507f055`

```dockerfile
```

-	Layers:
	-	`sha256:20273b8ec3e4c6442e0a5008f3f9ad0431185cd634d1d878c141a9574300d6e2`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 3.7 MB (3707850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8923fe4b3af6f27a6fae4be88118b6f5bbf9e79e928395bc3d20b86f013ac06`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.7.0`

```console
$ docker pull solr@sha256:4267344d8d37c5982894f8424e923a66e21461fc2d61602d935837d5d464182b
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
$ docker pull solr@sha256:c56b658c959f8ad2b7389d9b0107b48e3f95f13419788300f1f1297f198abdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.3 MB (375281077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d0bd9e56bc994ea086b4d7169937de4f8db32e98b1d481b13ec19856ebf830`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1aa583d1ef98fcaf42e21c147c70dd631fa34b36dc593c64265c54921dfd03`  
		Last Modified: Tue, 17 Sep 2024 01:58:19 GMT  
		Size: 283.1 MB (283083900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350cf53fd52a58d48f5d69688ffa4f77f51394ce81c3e6e81cb986dc1bba540d`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 4.3 KB (4270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b317c36e5a1025abf32228209e48b34ad153043e1bf9998c560e0b6e4e727164`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf7dd409191fcd1d9d51f54e8bfabeb0a53eca08b8da688a07588992f36b52c`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 10.9 KB (10867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24483e359719eee7ece7e8523546cd960c86efecf9b6990a080cbfdeb511ed1`  
		Last Modified: Tue, 17 Sep 2024 01:58:16 GMT  
		Size: 1.6 MB (1588536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0` - unknown; unknown

```console
$ docker pull solr@sha256:116ea6808bd356110ff347fb2574c286b721260a361f2e4ce35c6c678805e065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf593f0ad90c7de914051d98bb6b2ddf483c741f512f5d6842d0cc84b6e2af44`

```dockerfile
```

-	Layers:
	-	`sha256:77ffd5df8f3b12549b2e1216fd01df2f73b62374c87491ce014674f558833868`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 4.2 MB (4150903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c21b111477b68635e4f4ae71603feb8b8130a7feb123ba9b0d691d17b3ee7c55`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 34.0 KB (34047 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7.0` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:4ceca4ac998615dc3a80f7e67cf92dbd847e8e0bc04237f6f9f2928e75e82882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.5 MB (372505844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1026faf3194f8160c949410787ea9ffedf89e75772f25ecded9856195b0628e3`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257dbd9b6c377e0e75f4fe02716f6f373ee72cb589786a680f1100c695eaeb7a`  
		Last Modified: Tue, 17 Sep 2024 06:19:49 GMT  
		Size: 283.1 MB (283084078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f21f0a74e3bbc74b2541e017928f67aa6d3a04761bcf33faea7de058243d2c`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c12824d064498f7b2618f5c761d37409e87c6988cbc3b467b4c7f97e11fc5a1`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3aecd7313dcf51494ca18f98fb241d436e70d7b029239ba20b93d3d3d489b6`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 10.9 KB (10866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779e44c15834a5a622a574b87658e1eea3fe44616ee17308d5913942c21143fb`  
		Last Modified: Tue, 17 Sep 2024 06:19:45 GMT  
		Size: 1.4 MB (1447466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0` - unknown; unknown

```console
$ docker pull solr@sha256:e0a29761c26bec3ef130ef5c7d2d315ce715b0d10adaf2d1b1f01bd83b8c323a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4185560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d057f70f18b40b0e4d653edffbca453948a50642e3b3b73f3152c6e4785a342f`

```dockerfile
```

-	Layers:
	-	`sha256:0212511128601e44c88cca991fabc909ad9628577f68ee3d509facdb93f12d04`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 4.2 MB (4151196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b27012cb6170b8ae603f9c2a10a700f3e3b886e6ffcc9626104a9fb3fdb6481`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 34.4 KB (34364 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7.0` - linux; ppc64le

```console
$ docker pull solr@sha256:8b600bef8663026dc5874367d43a9c3b59236b3c75318ce6373ee4a2c20136eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381114029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09b1467a0770309e9acfdcac3b31cde50317cb57fb054cafc3e84e743017018`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2709165c356fd5bb9b4cda23232d8784bb71b95b05f605dc769df016474e33`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.1 MB (47115977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc5fce86e3a84ba35d6a9f9a976bd027569095ac890bb0a9be084a7b6d46a8e`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0e5434baa9330313b9e3fe8158f7e429b8e6f670f7827e3d0b7bf783db8f5`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9166f7814dcdbd5edcd0d198132f7d73400d07b553026275a8342b616828d4`  
		Last Modified: Tue, 17 Sep 2024 04:18:51 GMT  
		Size: 283.1 MB (283084447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fa47877401d2d997531c42aef453f1eedc981d83852613e4ffca8477d4dfc8`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 4.3 KB (4272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d41a688a4887ac1150669945f16640ce2f3ac7cf475e467466c3ef6a1c93388`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c4bd764cd9f26217ca67a27b61282e8017b5aacf46c492a07431fecbd6a45e`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 10.9 KB (10869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e3bd936391e4c95488f614d045b4a5051908e7a29245e0843e46cb0bbac3ba`  
		Last Modified: Tue, 17 Sep 2024 04:18:37 GMT  
		Size: 1.6 MB (1595531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0` - unknown; unknown

```console
$ docker pull solr@sha256:59588f3a8c982f85ce93be7a1d83ee2ecdc7d792b86d2e0eeff44ad435bdd32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953461ab2f2864fe202fd7a6d9870b694ab1e34170ea32e106993b64fe26425f`

```dockerfile
```

-	Layers:
	-	`sha256:6c494bbe8b57e7dd6714c1808135ff95ab2809e144769c06eddedf7bebae47ba`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 4.2 MB (4155429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e059d40138e1cee3c2b194f47ce62337b83272ba72e5d47b87ab59fbcf2f1e7a`  
		Last Modified: Tue, 17 Sep 2024 04:18:35 GMT  
		Size: 34.1 KB (34093 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7.0` - linux; s390x

```console
$ docker pull solr@sha256:0bd26f3815d4fbefdbc761da39c01cd601d74ee2b09555e49dc96d107fcbe1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370095765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3da1f9242c39468fe09d3e3fc38d13b71ff16f3bb82a6267fc404c9384f1c85`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd33900eddbaad7aef6f3b868400a94709edd5e4d439c0e7bf926ca7c34f184`  
		Last Modified: Tue, 17 Sep 2024 03:49:44 GMT  
		Size: 283.1 MB (283084224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d394f36e696d6e8145c7a7e05e50accc945e8347475575e3f8f3689b66646c8`  
		Last Modified: Tue, 17 Sep 2024 03:49:38 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b9a8d32862a02e8f90876527c50eea0d08b003a77bc1ed996341d57c4a206b`  
		Last Modified: Tue, 17 Sep 2024 03:49:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338736aa5b5c8d8c26d0208cd61c557a4ff9296d102001a445c72e802fcf10b6`  
		Last Modified: Tue, 17 Sep 2024 03:49:39 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95b165658950bff630dcbbedda6c18c58b3f786eda04774cd52c499e8b450ef`  
		Last Modified: Tue, 17 Sep 2024 03:49:40 GMT  
		Size: 1.5 MB (1535227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0` - unknown; unknown

```console
$ docker pull solr@sha256:077ce584ebc58a06dd0bfdd36085167a7b6e1c793ab986888f63446ca1cbd65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68118e13fe2e2840d191ff87b4cabfcf096b2764a3283fff584131964ae760c`

```dockerfile
```

-	Layers:
	-	`sha256:34f5f352acf6521c285cff397e1c9b7d735f1273e2a3d5e0455465e3a3974b1c`  
		Last Modified: Tue, 17 Sep 2024 03:49:39 GMT  
		Size: 4.2 MB (4152024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ecb0590de35c286840f10eeb7146a800dd09d72372f788ec9ea620e04b3319`  
		Last Modified: Tue, 17 Sep 2024 03:49:38 GMT  
		Size: 34.0 KB (34047 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:9.7.0-slim`

```console
$ docker pull solr@sha256:3191833409ac0349ebea8c9da9f2c8a0633ca67b184aeb1a36902e9b5d38539b
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
$ docker pull solr@sha256:5ff61de1418757425e028737bd010cb2a030b7a1955b8b9eea5de16a40f9ee9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157019263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb6986494c44f94ddfff0d1548a447d8fb79b7ecfa3559d8b2ccebc753753ea`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018cda53b3efa90b157c23cc92e3b69774f056abb446134fcbe3d15968857f5b`  
		Last Modified: Tue, 17 Sep 2024 01:58:08 GMT  
		Size: 64.8 MB (64822172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08103616a43c638c607be5d934ef046dc7bf8892966d0d961410f521e5a408f`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf3eabf6b02922222663f92fc056535dd5cd97dffb88684cfada2c309d3e9a5`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2fdc48848131a85389028e210f9f91b785eb6da8e2b928aebfa41cfab8261`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 10.8 KB (10782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec4a377ac5fd8f8ad2701146a5a77a47c863cc86c49c33b7028e3f178227759`  
		Last Modified: Tue, 17 Sep 2024 01:58:07 GMT  
		Size: 1.6 MB (1588526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:7c01207568df7fdc13030f0e12715086f630e571609daa9f21c3bf1109809bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe29adbd3d3ea2cf6b3227d2161d33bcd0cfda642f758da5a8ba5db7b05bd00`

```dockerfile
```

-	Layers:
	-	`sha256:2220b180518a4ec4985d4aba0ce5f4709142a2e133ffe6c9f51724b30f086261`  
		Last Modified: Tue, 17 Sep 2024 01:58:06 GMT  
		Size: 3.7 MB (3706729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43757148e05e2334fb7b85597007c07bc672e833ed833c9be2de45452ca9f8db`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7.0-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:195777fdbe8279808802bb4c2ff7b1041272f518a0f9159a332ff16d5a51f159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154244158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b542ab37706376e5ec336fe0a9b6b4caaaa37d4871b6e5056bd36db6068a3`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3acf7c85b7b1f4080586a56569199ed6f2666a97848ddf34af9b4e293115625`  
		Last Modified: Tue, 17 Sep 2024 06:20:40 GMT  
		Size: 64.8 MB (64822511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba76d9fa57a3a819707684b72833bd5aeefe6fc85ff3381d8e70dad81be1f757`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873080c20f3d3b7bdd26193c8dc28a1fd8e59f1bcbfdd76466cb23275c14d058`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630bf46d6ed4ff01c66668d72efe9a5a16e8687f695b1bc9d7b149102c059bfd`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 10.8 KB (10784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4d80fe3aa5c186c73106441598d6eb763e63207fbc6239f7dcb3a1224a3ce6`  
		Last Modified: Tue, 17 Sep 2024 06:20:40 GMT  
		Size: 1.4 MB (1447434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:97407c4de63b8e01b224ee43dd35888e107b73681c837cfa38244c92b6658873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525e5ee236c9c5a45c300ce639ed98156bce968bdf4ca90be36f6fc7c6b5b414`

```dockerfile
```

-	Layers:
	-	`sha256:feee39d2f9c4621a59b06a62cfc026ac84f2fd59fe467da055d5a4896f295df3`  
		Last Modified: Tue, 17 Sep 2024 06:20:39 GMT  
		Size: 3.7 MB (3707022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f5788cdf11a8e7fc232a9a7e986fee1e36af56c55e911982d495c24dbdc12d`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7.0-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:e474e41543c8a0f9d6c112656b3bc26c5ded6e7c7c877387fa247afe2dfdb728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162852273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cd1f1da329fdff8aa31f379d00d1a5f5f98a22361697b9188e7dcb7edc4641`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2709165c356fd5bb9b4cda23232d8784bb71b95b05f605dc769df016474e33`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.1 MB (47115977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc5fce86e3a84ba35d6a9f9a976bd027569095ac890bb0a9be084a7b6d46a8e`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0e5434baa9330313b9e3fe8158f7e429b8e6f670f7827e3d0b7bf783db8f5`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5cc63a136204177cb009444f1d4e30f778fa6342bc1fff3c415a2db26af859`  
		Last Modified: Tue, 17 Sep 2024 04:20:10 GMT  
		Size: 64.8 MB (64822807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f015af6089a3d3ce9ea59d066d6e2dfb91c3d75c469700392340d72a2cd9fb3`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 4.3 KB (4271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545d733fba4628b2bd6eac8273fb73a70b5ba52a64d8d929b83ecd8c6db0abba`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28954cd8d780db42f4455b9cd967947a7ccb6d8d238ae02092fa47cf80f3979f`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 10.8 KB (10787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c02cb793eafe46508fca732577230f3775f580de6283a3bef2bf557b2042a1`  
		Last Modified: Tue, 17 Sep 2024 04:20:09 GMT  
		Size: 1.6 MB (1595495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1e6d3fd4742692de1a98951978739b1424a65b1aacc6ae0274ee4c78aa185510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6632a300c80447bf453aa8a2d18ab3da903a6f2edd8f2fa73b4338503bab3d6`

```dockerfile
```

-	Layers:
	-	`sha256:466e5869a02f90160dd4ace6559b190ce24b3e1170f4b5245be5b7519f80dd99`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 3.7 MB (3711255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ec45fb6fec772aafb9e7bb001461fd296b07e2640a8da505888d788eaa2e4b`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 34.2 KB (34154 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9.7.0-slim` - linux; s390x

```console
$ docker pull solr@sha256:32aed8931be1df5fa8a4162fe06a48d6201aafb1ba297d28892987e501c8a5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151834055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a35a7e1018908896a4c1af9b4756ce7e9636fcb1561c19f630b9dd5a66a2c30`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2e4d148efe9b8ddc93fd95944cfa339847af273a2c1670177a272b9c577e49`  
		Last Modified: Tue, 17 Sep 2024 03:50:40 GMT  
		Size: 64.8 MB (64822613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de244efe4184c250f4ce53ad165d6e71af82b7a2d23601aefb5a7a5e2a08c098`  
		Last Modified: Tue, 17 Sep 2024 03:50:38 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75870b73c63df3e5916f4b20f3323eed537098164758505af69724e3eefe9b`  
		Last Modified: Tue, 17 Sep 2024 03:50:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dcf24f699c68c7dec74826b6f70798ec436579e1f7dd06eaaa1a8cf3cfe35a`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 10.8 KB (10784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319ac3aec22f66e31b317e2d05576e041647c7aa97cddc869c9a91a8366ef6d`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 1.5 MB (1535216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9.7.0-slim` - unknown; unknown

```console
$ docker pull solr@sha256:fac442f0523e1bb9886faace4e58d3b7cbc0683098f3de217f52c081df815a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b4502bc0be4c2e4b593a45180e288d60412f833f088ed4d31945adf507f055`

```dockerfile
```

-	Layers:
	-	`sha256:20273b8ec3e4c6442e0a5008f3f9ad0431185cd634d1d878c141a9574300d6e2`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 3.7 MB (3707850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8923fe4b3af6f27a6fae4be88118b6f5bbf9e79e928395bc3d20b86f013ac06`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:latest`

```console
$ docker pull solr@sha256:4267344d8d37c5982894f8424e923a66e21461fc2d61602d935837d5d464182b
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
$ docker pull solr@sha256:c56b658c959f8ad2b7389d9b0107b48e3f95f13419788300f1f1297f198abdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.3 MB (375281077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d0bd9e56bc994ea086b4d7169937de4f8db32e98b1d481b13ec19856ebf830`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1aa583d1ef98fcaf42e21c147c70dd631fa34b36dc593c64265c54921dfd03`  
		Last Modified: Tue, 17 Sep 2024 01:58:19 GMT  
		Size: 283.1 MB (283083900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350cf53fd52a58d48f5d69688ffa4f77f51394ce81c3e6e81cb986dc1bba540d`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 4.3 KB (4270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b317c36e5a1025abf32228209e48b34ad153043e1bf9998c560e0b6e4e727164`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf7dd409191fcd1d9d51f54e8bfabeb0a53eca08b8da688a07588992f36b52c`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 10.9 KB (10867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24483e359719eee7ece7e8523546cd960c86efecf9b6990a080cbfdeb511ed1`  
		Last Modified: Tue, 17 Sep 2024 01:58:16 GMT  
		Size: 1.6 MB (1588536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:116ea6808bd356110ff347fb2574c286b721260a361f2e4ce35c6c678805e065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4184950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf593f0ad90c7de914051d98bb6b2ddf483c741f512f5d6842d0cc84b6e2af44`

```dockerfile
```

-	Layers:
	-	`sha256:77ffd5df8f3b12549b2e1216fd01df2f73b62374c87491ce014674f558833868`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 4.2 MB (4150903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c21b111477b68635e4f4ae71603feb8b8130a7feb123ba9b0d691d17b3ee7c55`  
		Last Modified: Tue, 17 Sep 2024 01:58:15 GMT  
		Size: 34.0 KB (34047 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:4ceca4ac998615dc3a80f7e67cf92dbd847e8e0bc04237f6f9f2928e75e82882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.5 MB (372505844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1026faf3194f8160c949410787ea9ffedf89e75772f25ecded9856195b0628e3`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257dbd9b6c377e0e75f4fe02716f6f373ee72cb589786a680f1100c695eaeb7a`  
		Last Modified: Tue, 17 Sep 2024 06:19:49 GMT  
		Size: 283.1 MB (283084078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f21f0a74e3bbc74b2541e017928f67aa6d3a04761bcf33faea7de058243d2c`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c12824d064498f7b2618f5c761d37409e87c6988cbc3b467b4c7f97e11fc5a1`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3aecd7313dcf51494ca18f98fb241d436e70d7b029239ba20b93d3d3d489b6`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 10.9 KB (10866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779e44c15834a5a622a574b87658e1eea3fe44616ee17308d5913942c21143fb`  
		Last Modified: Tue, 17 Sep 2024 06:19:45 GMT  
		Size: 1.4 MB (1447466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:e0a29761c26bec3ef130ef5c7d2d315ce715b0d10adaf2d1b1f01bd83b8c323a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4185560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d057f70f18b40b0e4d653edffbca453948a50642e3b3b73f3152c6e4785a342f`

```dockerfile
```

-	Layers:
	-	`sha256:0212511128601e44c88cca991fabc909ad9628577f68ee3d509facdb93f12d04`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 4.2 MB (4151196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b27012cb6170b8ae603f9c2a10a700f3e3b886e6ffcc9626104a9fb3fdb6481`  
		Last Modified: Tue, 17 Sep 2024 06:19:44 GMT  
		Size: 34.4 KB (34364 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:8b600bef8663026dc5874367d43a9c3b59236b3c75318ce6373ee4a2c20136eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381114029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09b1467a0770309e9acfdcac3b31cde50317cb57fb054cafc3e84e743017018`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2709165c356fd5bb9b4cda23232d8784bb71b95b05f605dc769df016474e33`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.1 MB (47115977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc5fce86e3a84ba35d6a9f9a976bd027569095ac890bb0a9be084a7b6d46a8e`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0e5434baa9330313b9e3fe8158f7e429b8e6f670f7827e3d0b7bf783db8f5`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9166f7814dcdbd5edcd0d198132f7d73400d07b553026275a8342b616828d4`  
		Last Modified: Tue, 17 Sep 2024 04:18:51 GMT  
		Size: 283.1 MB (283084447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fa47877401d2d997531c42aef453f1eedc981d83852613e4ffca8477d4dfc8`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 4.3 KB (4272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d41a688a4887ac1150669945f16640ce2f3ac7cf475e467466c3ef6a1c93388`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c4bd764cd9f26217ca67a27b61282e8017b5aacf46c492a07431fecbd6a45e`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 10.9 KB (10869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e3bd936391e4c95488f614d045b4a5051908e7a29245e0843e46cb0bbac3ba`  
		Last Modified: Tue, 17 Sep 2024 04:18:37 GMT  
		Size: 1.6 MB (1595531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:59588f3a8c982f85ce93be7a1d83ee2ecdc7d792b86d2e0eeff44ad435bdd32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953461ab2f2864fe202fd7a6d9870b694ab1e34170ea32e106993b64fe26425f`

```dockerfile
```

-	Layers:
	-	`sha256:6c494bbe8b57e7dd6714c1808135ff95ab2809e144769c06eddedf7bebae47ba`  
		Last Modified: Tue, 17 Sep 2024 04:18:36 GMT  
		Size: 4.2 MB (4155429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e059d40138e1cee3c2b194f47ce62337b83272ba72e5d47b87ab59fbcf2f1e7a`  
		Last Modified: Tue, 17 Sep 2024 04:18:35 GMT  
		Size: 34.1 KB (34093 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:0bd26f3815d4fbefdbc761da39c01cd601d74ee2b09555e49dc96d107fcbe1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370095765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3da1f9242c39468fe09d3e3fc38d13b71ff16f3bb82a6267fc404c9384f1c85`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd33900eddbaad7aef6f3b868400a94709edd5e4d439c0e7bf926ca7c34f184`  
		Last Modified: Tue, 17 Sep 2024 03:49:44 GMT  
		Size: 283.1 MB (283084224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d394f36e696d6e8145c7a7e05e50accc945e8347475575e3f8f3689b66646c8`  
		Last Modified: Tue, 17 Sep 2024 03:49:38 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b9a8d32862a02e8f90876527c50eea0d08b003a77bc1ed996341d57c4a206b`  
		Last Modified: Tue, 17 Sep 2024 03:49:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338736aa5b5c8d8c26d0208cd61c557a4ff9296d102001a445c72e802fcf10b6`  
		Last Modified: Tue, 17 Sep 2024 03:49:39 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95b165658950bff630dcbbedda6c18c58b3f786eda04774cd52c499e8b450ef`  
		Last Modified: Tue, 17 Sep 2024 03:49:40 GMT  
		Size: 1.5 MB (1535227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:077ce584ebc58a06dd0bfdd36085167a7b6e1c793ab986888f63446ca1cbd65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4186071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68118e13fe2e2840d191ff87b4cabfcf096b2764a3283fff584131964ae760c`

```dockerfile
```

-	Layers:
	-	`sha256:34f5f352acf6521c285cff397e1c9b7d735f1273e2a3d5e0455465e3a3974b1c`  
		Last Modified: Tue, 17 Sep 2024 03:49:39 GMT  
		Size: 4.2 MB (4152024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7ecb0590de35c286840f10eeb7146a800dd09d72372f788ec9ea620e04b3319`  
		Last Modified: Tue, 17 Sep 2024 03:49:38 GMT  
		Size: 34.0 KB (34047 bytes)  
		MIME: application/vnd.in-toto+json

## `solr:slim`

```console
$ docker pull solr@sha256:3191833409ac0349ebea8c9da9f2c8a0633ca67b184aeb1a36902e9b5d38539b
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
$ docker pull solr@sha256:5ff61de1418757425e028737bd010cb2a030b7a1955b8b9eea5de16a40f9ee9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157019263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb6986494c44f94ddfff0d1548a447d8fb79b7ecfa3559d8b2ccebc753753ea`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018cda53b3efa90b157c23cc92e3b69774f056abb446134fcbe3d15968857f5b`  
		Last Modified: Tue, 17 Sep 2024 01:58:08 GMT  
		Size: 64.8 MB (64822172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08103616a43c638c607be5d934ef046dc7bf8892966d0d961410f521e5a408f`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf3eabf6b02922222663f92fc056535dd5cd97dffb88684cfada2c309d3e9a5`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2fdc48848131a85389028e210f9f91b785eb6da8e2b928aebfa41cfab8261`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 10.8 KB (10782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec4a377ac5fd8f8ad2701146a5a77a47c863cc86c49c33b7028e3f178227759`  
		Last Modified: Tue, 17 Sep 2024 01:58:07 GMT  
		Size: 1.6 MB (1588526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:7c01207568df7fdc13030f0e12715086f630e571609daa9f21c3bf1109809bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe29adbd3d3ea2cf6b3227d2161d33bcd0cfda642f758da5a8ba5db7b05bd00`

```dockerfile
```

-	Layers:
	-	`sha256:2220b180518a4ec4985d4aba0ce5f4709142a2e133ffe6c9f51724b30f086261`  
		Last Modified: Tue, 17 Sep 2024 01:58:06 GMT  
		Size: 3.7 MB (3706729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43757148e05e2334fb7b85597007c07bc672e833ed833c9be2de45452ca9f8db`  
		Last Modified: Tue, 17 Sep 2024 01:58:05 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:195777fdbe8279808802bb4c2ff7b1041272f518a0f9159a332ff16d5a51f159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154244158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b542ab37706376e5ec336fe0a9b6b4caaaa37d4871b6e5056bd36db6068a3`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3acf7c85b7b1f4080586a56569199ed6f2666a97848ddf34af9b4e293115625`  
		Last Modified: Tue, 17 Sep 2024 06:20:40 GMT  
		Size: 64.8 MB (64822511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba76d9fa57a3a819707684b72833bd5aeefe6fc85ff3381d8e70dad81be1f757`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873080c20f3d3b7bdd26193c8dc28a1fd8e59f1bcbfdd76466cb23275c14d058`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630bf46d6ed4ff01c66668d72efe9a5a16e8687f695b1bc9d7b149102c059bfd`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 10.8 KB (10784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4d80fe3aa5c186c73106441598d6eb763e63207fbc6239f7dcb3a1224a3ce6`  
		Last Modified: Tue, 17 Sep 2024 06:20:40 GMT  
		Size: 1.4 MB (1447434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:97407c4de63b8e01b224ee43dd35888e107b73681c837cfa38244c92b6658873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525e5ee236c9c5a45c300ce639ed98156bce968bdf4ca90be36f6fc7c6b5b414`

```dockerfile
```

-	Layers:
	-	`sha256:feee39d2f9c4621a59b06a62cfc026ac84f2fd59fe467da055d5a4896f295df3`  
		Last Modified: Tue, 17 Sep 2024 06:20:39 GMT  
		Size: 3.7 MB (3707022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f5788cdf11a8e7fc232a9a7e986fee1e36af56c55e911982d495c24dbdc12d`  
		Last Modified: Tue, 17 Sep 2024 06:20:38 GMT  
		Size: 34.4 KB (34427 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; ppc64le

```console
$ docker pull solr@sha256:e474e41543c8a0f9d6c112656b3bc26c5ded6e7c7c877387fa247afe2dfdb728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162852273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cd1f1da329fdff8aa31f379d00d1a5f5f98a22361697b9188e7dcb7edc4641`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2709165c356fd5bb9b4cda23232d8784bb71b95b05f605dc769df016474e33`  
		Last Modified: Tue, 17 Sep 2024 01:09:11 GMT  
		Size: 47.1 MB (47115977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc5fce86e3a84ba35d6a9f9a976bd027569095ac890bb0a9be084a7b6d46a8e`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0e5434baa9330313b9e3fe8158f7e429b8e6f670f7827e3d0b7bf783db8f5`  
		Last Modified: Tue, 17 Sep 2024 01:09:03 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5cc63a136204177cb009444f1d4e30f778fa6342bc1fff3c415a2db26af859`  
		Last Modified: Tue, 17 Sep 2024 04:20:10 GMT  
		Size: 64.8 MB (64822807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f015af6089a3d3ce9ea59d066d6e2dfb91c3d75c469700392340d72a2cd9fb3`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 4.3 KB (4271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545d733fba4628b2bd6eac8273fb73a70b5ba52a64d8d929b83ecd8c6db0abba`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28954cd8d780db42f4455b9cd967947a7ccb6d8d238ae02092fa47cf80f3979f`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 10.8 KB (10787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c02cb793eafe46508fca732577230f3775f580de6283a3bef2bf557b2042a1`  
		Last Modified: Tue, 17 Sep 2024 04:20:09 GMT  
		Size: 1.6 MB (1595495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:1e6d3fd4742692de1a98951978739b1424a65b1aacc6ae0274ee4c78aa185510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6632a300c80447bf453aa8a2d18ab3da903a6f2edd8f2fa73b4338503bab3d6`

```dockerfile
```

-	Layers:
	-	`sha256:466e5869a02f90160dd4ace6559b190ce24b3e1170f4b5245be5b7519f80dd99`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 3.7 MB (3711255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ec45fb6fec772aafb9e7bb001461fd296b07e2640a8da505888d788eaa2e4b`  
		Last Modified: Tue, 17 Sep 2024 04:20:07 GMT  
		Size: 34.2 KB (34154 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:slim` - linux; s390x

```console
$ docker pull solr@sha256:32aed8931be1df5fa8a4162fe06a48d6201aafb1ba297d28892987e501c8a5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151834055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a35a7e1018908896a4c1af9b4756ce7e9636fcb1561c19f630b9dd5a66a2c30`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4624ad96cbf703fad2edcc0005acc9749c20d1225e6b1448c6dd8e9ac9804ee5`  
		Last Modified: Tue, 17 Sep 2024 01:40:26 GMT  
		Size: 43.9 MB (43864187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b482022d8f8067a28d53d22a86ce7b37f78ccfee8cb5702b8b1194829920bca`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4228af43016bae62a4197267666f007e8f88917ce953bc7e3aef105c2b4cc9`  
		Last Modified: Tue, 17 Sep 2024 01:40:20 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2e4d148efe9b8ddc93fd95944cfa339847af273a2c1670177a272b9c577e49`  
		Last Modified: Tue, 17 Sep 2024 03:50:40 GMT  
		Size: 64.8 MB (64822613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de244efe4184c250f4ce53ad165d6e71af82b7a2d23601aefb5a7a5e2a08c098`  
		Last Modified: Tue, 17 Sep 2024 03:50:38 GMT  
		Size: 4.3 KB (4304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75870b73c63df3e5916f4b20f3323eed537098164758505af69724e3eefe9b`  
		Last Modified: Tue, 17 Sep 2024 03:50:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dcf24f699c68c7dec74826b6f70798ec436579e1f7dd06eaaa1a8cf3cfe35a`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 10.8 KB (10784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c319ac3aec22f66e31b317e2d05576e041647c7aa97cddc869c9a91a8366ef6d`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 1.5 MB (1535216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:slim` - unknown; unknown

```console
$ docker pull solr@sha256:fac442f0523e1bb9886faace4e58d3b7cbc0683098f3de217f52c081df815a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b4502bc0be4c2e4b593a45180e288d60412f833f088ed4d31945adf507f055`

```dockerfile
```

-	Layers:
	-	`sha256:20273b8ec3e4c6442e0a5008f3f9ad0431185cd634d1d878c141a9574300d6e2`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 3.7 MB (3707850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8923fe4b3af6f27a6fae4be88118b6f5bbf9e79e928395bc3d20b86f013ac06`  
		Last Modified: Tue, 17 Sep 2024 03:50:39 GMT  
		Size: 34.1 KB (34110 bytes)  
		MIME: application/vnd.in-toto+json
