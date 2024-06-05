## `solr:8-slim`

```console
$ docker pull solr@sha256:ddf4162f4e36d3d1ba88aae08a629aeec9370589486c41e6fe271b9c30ba5226
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
$ docker pull solr@sha256:150d93b3bb6dd3951b28d3112e7cb3f2a096b6fa0135dcda87bcec97b90e5e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322507823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9363203e63328ec0e9787e8cccdb169149441decbd921a97dbcb2bfdb5c7d8a`
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
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='025f994549708f7291ce3b0fa7c41f7e78ec3af3eae3f85fffe9c5fa4a54889f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef1f9e9d220aa4c081924e26f514bbafee5fecb9cb7f8e3b5b19762ce947fa`  
		Last Modified: Wed, 05 Jun 2024 04:57:49 GMT  
		Size: 16.9 MB (16920774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d12eb8458375092df4e2493012a51084e9f7c417a4fc4b8acf1c82d763b2ea6`  
		Last Modified: Wed, 05 Jun 2024 04:59:46 GMT  
		Size: 47.2 MB (47184661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6b831a8af99635c978bbfdcd331f295d19a889b7c2bc9d32453b92bba07550`  
		Last Modified: Wed, 05 Jun 2024 04:59:40 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263fced69c600ea31503c2bc564243ad0af9d3e44eb56c5bac482654262a2ce8`  
		Last Modified: Wed, 05 Jun 2024 04:59:40 GMT  
		Size: 732.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e550b43ff6f6f9980d534987afac6a4724bfdf01d70499d11c52b369bf63e23`  
		Last Modified: Wed, 05 Jun 2024 06:11:05 GMT  
		Size: 4.7 MB (4663725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcb720819d30046119891b25077bc0fad91e410a0f3d4e20c8b23ae3417a7f`  
		Last Modified: Wed, 05 Jun 2024 06:11:05 GMT  
		Size: 4.3 KB (4270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88982fd1d49a4afac980001ec78a5407f7949b2629c987106b7625f695a60315`  
		Last Modified: Wed, 05 Jun 2024 06:11:05 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a46c38ebf960b9929fd28287899bc66380fa180734faccefd313c05214f958e`  
		Last Modified: Wed, 05 Jun 2024 06:11:09 GMT  
		Size: 225.1 MB (225140081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1189a45ec269d03942a651c61f61a11b9fdc58b37b0365b7a116a0ec86925d58`  
		Last Modified: Wed, 05 Jun 2024 06:11:06 GMT  
		Size: 6.3 KB (6277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:c2a9a926a92cf41f6539469b61e44ffe9550b54422705957f7f3d2802967792c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6894f7b73a598ee1e70f622d8b59b9b91b160b2ae443680bfc44259d8343b79d`

```dockerfile
```

-	Layers:
	-	`sha256:fb13ed0255c423a597ddbf7f3f703ca4c10d9c09ddbd385c431e719a6f6f6a2f`  
		Last Modified: Wed, 05 Jun 2024 06:11:05 GMT  
		Size: 4.0 MB (3983868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73306ed65e1983df8244a99562c716017608ccebbaf073bad8455471668740f9`  
		Last Modified: Wed, 05 Jun 2024 06:11:05 GMT  
		Size: 36.3 KB (36299 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:d7b8e61cd43b02751cd50d37adb7e0f419c070189da67d6ff07df7f7171fc6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.2 MB (319206951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889590a932700878d28d7ac27e231b1ec608025c3e4c6102dc2abc6055ca2cfe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='025f994549708f7291ce3b0fa7c41f7e78ec3af3eae3f85fffe9c5fa4a54889f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Sat, 27 Apr 2024 18:14:55 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_VERSION=8.11.3
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_DOWNLOAD_URL
# Sat, 27 Apr 2024 18:14:55 GMT
ARG SOLR_DOWNLOAD_SERVER
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512 # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=https://www.apache.org/dyn/closer.lua/lucene/solr/8.11.3/solr-8.11.3.tgz?action=download SOLR_DIST_URL=https://downloads.apache.org/lucene/solr/8.11.3/solr-8.11.3.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.3/solr-8.11.3.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0 # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME" # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
COPY --chown=0:0 scripts /opt/docker-solr/scripts # buildkit
# Sat, 27 Apr 2024 18:14:55 GMT
VOLUME [/var/solr]
# Sat, 27 Apr 2024 18:14:55 GMT
EXPOSE map[8983/tcp:{}]
# Sat, 27 Apr 2024 18:14:55 GMT
WORKDIR /opt/solr
# Sat, 27 Apr 2024 18:14:55 GMT
USER 8983
# Sat, 27 Apr 2024 18:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Apr 2024 18:14:55 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3510597c9954b37f646e357b476e00ba683391a190199312f9fd3f1344ca2d`  
		Last Modified: Thu, 02 May 2024 04:17:12 GMT  
		Size: 16.8 MB (16777842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057caf1047012c9c5382e121bd40eda49ae53d504bd614a9afc3eaacb6f73fdc`  
		Last Modified: Thu, 02 May 2024 04:18:59 GMT  
		Size: 45.6 MB (45556231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ffac78cac2a5061f80b6db39ac041aeb36282c28ced0c3c208c617210ce1bc`  
		Last Modified: Thu, 02 May 2024 04:18:54 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9129110deb659be153049e48f58a825d9b6e23ec551c5ea0d49b9779de66c942`  
		Last Modified: Thu, 02 May 2024 04:18:54 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb4ff7f4872a1be906b34f7e5bcfaac73cc73fcc5a92b0215ac2455d3783cb7`  
		Last Modified: Mon, 06 May 2024 16:54:39 GMT  
		Size: 4.5 MB (4512210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3697ca8718020489a89c8fa2222112901b9c379be5e44e5f2d1f4cb7881c666`  
		Last Modified: Mon, 06 May 2024 16:54:39 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ddd0e862ccf7ddf2d6f7c6222cf43ee2f60af67108ba2bcf99a70811142e47`  
		Last Modified: Mon, 06 May 2024 16:54:39 GMT  
		Size: 2.9 KB (2886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3339246866aa2895335187585cb0acdab2e93aa3efda8f32dfa50c0d447019e4`  
		Last Modified: Mon, 06 May 2024 16:54:44 GMT  
		Size: 225.1 MB (225140136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6041000fd88d620fc2091305674932862570c480f949f32170e1cb4ad78eef`  
		Last Modified: Mon, 06 May 2024 16:54:40 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:1223a9b7317327f3038f5597c4c6222f362ac1f38871aa6be74e870f43ecaab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e645f464f61190f761e89f8f6d20d9588136e608ddd3c0779d25365cf67092`

```dockerfile
```

-	Layers:
	-	`sha256:12882ae9b2e97165bdb6d908dfab1032b95224227de55e8d29ebe2066edaad07`  
		Last Modified: Mon, 06 May 2024 16:55:04 GMT  
		Size: 4.0 MB (3984100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d538fd916014e591a26aa1afc46b04c8ef27bbc81344e2c1af4b6cafc764a37`  
		Last Modified: Mon, 06 May 2024 16:55:03 GMT  
		Size: 36.3 KB (36307 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:61df97480d2a6a1b5e5fc798a3e463c7b24a14830c16495863e1d79fbe1698be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324871954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8f757855e1444c38cc3230caaa838b819674b3a94c0e1263c278db9b3db5e8`
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
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='025f994549708f7291ce3b0fa7c41f7e78ec3af3eae3f85fffe9c5fa4a54889f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef025249b0fe621dd5c39de7e56c0ca2be3a550f30946c0103b22cfb65ce0adf`  
		Last Modified: Wed, 05 Jun 2024 04:00:00 GMT  
		Size: 18.2 MB (18222028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c7e2693131c3a395a2782eb8771b8be47aba07f1cc0ee0f50afaf75b041021`  
		Last Modified: Wed, 05 Jun 2024 04:01:56 GMT  
		Size: 42.6 MB (42639262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b630ee21c751e1dd65914fe1bb0ad014d62872ed7846e28b063c69ef5219ac0a`  
		Last Modified: Wed, 05 Jun 2024 04:01:50 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a714bdb033234c0792bb07cffd25d393c9417639f288983592d19023bbcc4b52`  
		Last Modified: Wed, 05 Jun 2024 04:01:50 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d5060052330727bd40ceed6f77f8b4fd1441a760c2e69a931f6e1ce5d46105`  
		Last Modified: Wed, 05 Jun 2024 15:18:54 GMT  
		Size: 5.5 MB (5539889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43dccd0319a41bfadfbb164675b1dfb2ab2f77ad861fe468b672d3c2aff12e1`  
		Last Modified: Wed, 05 Jun 2024 15:18:54 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbdfe98a34ddd10ce7609483eb1600463a8ccf41a83b3e8bd14c2e7388f1494`  
		Last Modified: Wed, 05 Jun 2024 15:18:54 GMT  
		Size: 2.9 KB (2890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab215116e5888f0f1b43ec20002ef60435e9b7760a406ee6e6b876ea93d4328`  
		Last Modified: Wed, 05 Jun 2024 15:19:00 GMT  
		Size: 225.1 MB (225140292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34535ce1d16c9b6d6900b0a56fa3f3e9a3e9b00a60f11bec499b6474744911b0`  
		Last Modified: Wed, 05 Jun 2024 15:18:55 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:fa410060a57c7fad2ed5bfbfe6d498fa2eb123891107e6dc2fb6b0d8897a2a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6961d1cb3df110a4f7ff2806c2edeb1437ff04798757e3f739d060d92632ec`

```dockerfile
```

-	Layers:
	-	`sha256:026494db8b95fcb60e2db82d72b2585bc613b8ec684cee2b4109d502e5eefa73`  
		Last Modified: Wed, 05 Jun 2024 15:19:23 GMT  
		Size: 4.0 MB (3988361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:217b5e634c77053aeb5ac8f8f1f49b69adb62c28b553048b3c338eda636d78b9`  
		Last Modified: Wed, 05 Jun 2024 15:19:22 GMT  
		Size: 36.3 KB (36336 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; s390x

```console
$ docker pull solr@sha256:70aba714c5d026508daa7b7838f43b33df4bd7e0169803fcf788b8c87f0544d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314106672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fc202f621cd28562ae897ee4c30711d0576523f14221cdf4e8301370c961ef`
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
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
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
ENV JAVA_VERSION=jdk-11.0.23+9
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='025f994549708f7291ce3b0fa7c41f7e78ec3af3eae3f85fffe9c5fa4a54889f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
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
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a156a04bb486c4a1c69c74a9f01dce29f2e013ccab4e6631197f6cc4d8f4c45`  
		Last Modified: Wed, 05 Jun 2024 03:12:17 GMT  
		Size: 16.6 MB (16645456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d1f5258203381bb0e1420f82764369f45a54dd35c2626cc86f85a2b62f2032`  
		Last Modified: Wed, 05 Jun 2024 03:12:59 GMT  
		Size: 40.8 MB (40800357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a4a6ffd93db310536ba7d14c0ef8fcabc6704b4c8f7d62e01cda5fa0122934`  
		Last Modified: Wed, 05 Jun 2024 03:12:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a148af8602027da6b902c804510231dd7daaa0d90eb4616a6a772457e06bdfd`  
		Last Modified: Wed, 05 Jun 2024 03:12:54 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8c5e8f2b4f3992581bd47079e59bb5aa0d26b88dec4d7728261e500a476bf3`  
		Last Modified: Wed, 05 Jun 2024 08:27:38 GMT  
		Size: 4.5 MB (4492854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73264c70a6b0998a6a3b4566592b317fb75a05320b0f92bd1ce9b36a32a7250`  
		Last Modified: Wed, 05 Jun 2024 08:27:39 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a72c98211b4531b43ea60f78935e23ee0e7bc203e1baae644fffe20d259daa`  
		Last Modified: Wed, 05 Jun 2024 08:27:39 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ea0fbb60294c0cae1f8a95f2a167ba821521bcd252245f57e13f361217cfa9`  
		Last Modified: Wed, 05 Jun 2024 08:27:44 GMT  
		Size: 225.1 MB (225140185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36811e3c89224896be87e64cf9bb46c77980809d770b69d232ac3b028f92787`  
		Last Modified: Wed, 05 Jun 2024 08:27:39 GMT  
		Size: 6.3 KB (6279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:b53e0f5a82fca0687980e21fdf51f1c17406d637b647515a9b74660b3441b824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a61a48148a1239e84d992ae73b683c9cc8361bd9d2b8efc91aa07857d40a232`

```dockerfile
```

-	Layers:
	-	`sha256:8d57598f1d12129a23c7c153fc9c67fbf2f192a87db0db997890d18c6201d133`  
		Last Modified: Wed, 05 Jun 2024 08:28:13 GMT  
		Size: 4.0 MB (3984304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d25b703e278e6427a0ed12e13ba852ca1840bf765891eab756450a81dad36666`  
		Last Modified: Wed, 05 Jun 2024 08:28:13 GMT  
		Size: 36.3 KB (36297 bytes)  
		MIME: application/vnd.in-toto+json
