## `solr:8-slim`

```console
$ docker pull solr@sha256:7646fcd37d69cbcbe0e5ad570666603f81e68d8cd89b710efd2ebda45f3bb8bf
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
$ docker pull solr@sha256:c8304b4239191a8c8242aadfd304f151f2e838ff9d58f8715681cd70fa610f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.9 MB (322860430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f29c86a9e5b34d7b4b3ebf2fd3ea81d2ebb7a67788b344f6820a9b7861792c`
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:65c79716ce2573e0cd3464a688211336d1ee703c3eef803ae4cf3438e0c64272`  
		Last Modified: Wed, 24 Jul 2024 01:28:16 GMT  
		Size: 47.2 MB (47196864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cffdbb20fcf65eb28ccf57ec92b97ed19233b4e2b7bd740b0fb41b6b8de2514`  
		Last Modified: Wed, 24 Jul 2024 01:28:10 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4732c6541e945015f6daeedf7d41cb6a1260802b2f0304454064853db27e6a6`  
		Last Modified: Thu, 25 Jul 2024 17:28:58 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872c2dd4306ed16e456895aa1534c5fec59bc4be30a6f99c1ffed6ec7430a4bd`  
		Last Modified: Thu, 25 Jul 2024 19:03:26 GMT  
		Size: 5.0 MB (5002672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e654c4e62547f6841f9f09cfcd32dde5befe790caf37ddf2a3122beea93d81e`  
		Last Modified: Thu, 25 Jul 2024 19:03:25 GMT  
		Size: 4.3 KB (4276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82d4e4bb5f4857f626c4f8bd884c8b299197b25e350f2d3be46d9ee9f2ad828`  
		Last Modified: Thu, 25 Jul 2024 19:03:26 GMT  
		Size: 2.9 KB (2891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580e6958de1922c5bcf41e2107bc6588a80fac0efa386e4c8e337adcb3fe2ed3`  
		Last Modified: Thu, 25 Jul 2024 19:03:31 GMT  
		Size: 225.1 MB (225140403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7562bd906ac1f3e0759da33bf7695a52db41ad6bca33df5fd0fa47c496e1038`  
		Last Modified: Thu, 25 Jul 2024 19:03:26 GMT  
		Size: 6.3 KB (6271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:55096ddac4c87426ac4702fc0adcca82eaab3faa4169b88489583897324ef52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4093529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a0616e43fbc861960683181962266d0810cb3d262e80d66542c152612d6fee`

```dockerfile
```

-	Layers:
	-	`sha256:359c4f99c72644760e091ac375510453d5fad9fb3f4fd17528b5cc133dd102e1`  
		Last Modified: Thu, 25 Jul 2024 19:03:25 GMT  
		Size: 4.1 MB (4057174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cbb505b845541e4bc1b11ef7afddc2f8d4a7323b77933d80d1581f4b694d2a4`  
		Last Modified: Thu, 25 Jul 2024 19:03:25 GMT  
		Size: 36.4 KB (36355 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:2094ed62a3a56acd0d51b9afc101cb0c08feb252438477c85230cb86286663f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319543179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b94bbeec4afe8e51b0248f136bd34c0c259ad506214c81bb0854f82a7484f8`
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
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:ab086bee7343f77e1230a759e5b2224cb3ca5b07e8459713b044887708f7b89a`  
		Last Modified: Thu, 25 Jul 2024 17:45:15 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93faebba967e3366a7fbadc3c3b46d4439e1da0f7709034a87b3671da8d7d2`  
		Last Modified: Thu, 25 Jul 2024 22:39:11 GMT  
		Size: 4.8 MB (4847778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0a648402619f3dd35d190348ff0fdcf5de2c5e4df7774ddb133a20652e209e`  
		Last Modified: Thu, 25 Jul 2024 22:39:11 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013f512207fd469e313844f269994c3cfb137d3a6a8ddecf64111a9e0f82a185`  
		Last Modified: Thu, 25 Jul 2024 22:39:11 GMT  
		Size: 2.9 KB (2892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641ed57754e6c98b23a00c5270081386016da1043b5f5090e6ba6359fe492891`  
		Last Modified: Thu, 25 Jul 2024 22:39:16 GMT  
		Size: 225.1 MB (225140406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d4afa0e513902368570337e8912461b68c915ac60ed3a905bd53fe062454f4`  
		Last Modified: Thu, 25 Jul 2024 22:39:12 GMT  
		Size: 6.3 KB (6273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:63a0c63f394ad1e507e12f2632238f0ffaacdec010630f7fdbdc346a09fa3aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4094077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021d1ce8716b13a9f8e76b4acc9b9a9af8864b10f97e3e26ca3943157d143fa0`

```dockerfile
```

-	Layers:
	-	`sha256:c7e6e541710c9061b6ca460c6898b7366fcf673bd0a0dc9d257bfad001f90764`  
		Last Modified: Thu, 25 Jul 2024 22:39:36 GMT  
		Size: 4.1 MB (4057417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14c9f53aa489279c4f82c57f1ccfc387f9adbc3a5b4a2217bce48b43439ff555`  
		Last Modified: Thu, 25 Jul 2024 22:39:36 GMT  
		Size: 36.7 KB (36660 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:4ce11ea62ce86ce6259ebb3300da8ffb09e6d2bf6d1423e9471961af7c5ef943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325287265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf9d5899b5021e09900d85aab2cafe024749311e61a0f5070f819c004596d1a`
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:909ebbc0bdbd07a40e729bb5b958f22d12e3d154aded190a6cc48e187be81dda`  
		Last Modified: Wed, 24 Jul 2024 04:13:08 GMT  
		Size: 42.7 MB (42652860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f0c163d60b8d17f187a1ce7c28da5c01c3d9a83bde0f609ee802566ab0e06`  
		Last Modified: Wed, 24 Jul 2024 04:13:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f5f3f93dae2ef80c2248d70922a3468e9a59456abe2fe93b86a0969f31f2fa`  
		Last Modified: Thu, 25 Jul 2024 17:24:21 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27a51e2443d0a63f9f650e4d2b269596117011560e4557c934bcf9aa8f70009`  
		Last Modified: Thu, 25 Jul 2024 19:50:29 GMT  
		Size: 5.9 MB (5940409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95debbc6deb1549cd3bd24841648edc0f350a95cad9ef62f4b8168a65be358f0`  
		Last Modified: Thu, 25 Jul 2024 19:50:29 GMT  
		Size: 4.3 KB (4279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f7d5576482e3a757dbde4c41b871f1b9306323ab239732b27bd1b4fd99585c`  
		Last Modified: Thu, 25 Jul 2024 19:50:29 GMT  
		Size: 2.9 KB (2889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4adb6146c60ccab10b96b925eead7cb538060fd58a8c2feb3a5783d437eebb1`  
		Last Modified: Thu, 25 Jul 2024 19:50:36 GMT  
		Size: 225.1 MB (225140346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aac991bcc3bb73c7221232e29bc5266c5181e81ce0959e45db072904b25adb6`  
		Last Modified: Thu, 25 Jul 2024 19:50:30 GMT  
		Size: 6.3 KB (6277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:ecf942cc3ab42ef2ec541b29deb0f3994397f984c99cf36fb2ec96c654da369a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce05bc7f6de1761bc4168553ad1c21a3832b16e86df52ffde20c4929dcbd1737`

```dockerfile
```

-	Layers:
	-	`sha256:306fb05e7b3c0f3c4f337ade01ce118397ce6c57660ae439be2013db11fb722d`  
		Last Modified: Thu, 25 Jul 2024 19:51:03 GMT  
		Size: 4.1 MB (4061667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3660d269618aaa66ab3ca9883da6d427ab2ec7a7439b17cd7f24f9d6115052`  
		Last Modified: Thu, 25 Jul 2024 19:51:02 GMT  
		Size: 36.4 KB (36393 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; s390x

```console
$ docker pull solr@sha256:7d1c06d23e7f548c5896b7ee112cfd88c871906ec1de3378491e988d85fdb444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 MB (314464281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c9c1da179753b3e2e74bfbe5c1e2aad60bb19fdd0ed500691631ee72ea7f9b8`
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
ENV JAVA_VERSION=jdk-11.0.24+8
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='bf893085627c6ec484e63aa1290276b23bcfee547459da6b0432ae9c5c1be22a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 09 Feb 2024 17:48:20 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
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
	-	`sha256:dd37eed98237b35cbfd9c26e61e50843a3e5cd2ebf664c58e31194178944624f`  
		Last Modified: Wed, 24 Jul 2024 00:57:17 GMT  
		Size: 40.8 MB (40818422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6348169ce0d5dbce34a24949a87f35c57f8e5f9d5b1913297de765327f3c20fd`  
		Last Modified: Wed, 24 Jul 2024 00:57:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ed93115516b2b372b1461a72c74e29cc4ae743bda099b5a3926f4b07dd05b8`  
		Last Modified: Thu, 25 Jul 2024 17:48:01 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec83ce8e9cde5daef138a080c9745d3aee4796eadebc7d4f54e897596731c3fd`  
		Last Modified: Thu, 25 Jul 2024 19:29:29 GMT  
		Size: 4.8 MB (4831206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d67158b242e691d3469a4f337e881822ca3505a6228bf6f56b2d70f4a6d9433`  
		Last Modified: Thu, 25 Jul 2024 19:29:28 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728a5a838482878277487f102a4381457d826f32ed5df3960affc8e596b88519`  
		Last Modified: Thu, 25 Jul 2024 19:29:28 GMT  
		Size: 2.9 KB (2890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d606f6509c37c3238132bf0952f675b293ee4778082aff17936094413d3c46`  
		Last Modified: Thu, 25 Jul 2024 19:29:32 GMT  
		Size: 225.1 MB (225140249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efffdf207ca423f1df5982d7c753a04bb3b22c74f1b45354445111cf43712e0`  
		Last Modified: Thu, 25 Jul 2024 19:29:29 GMT  
		Size: 6.3 KB (6273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:954a113b0e4d80e180df318872bb0f64b15f4e0531d9d78c1a69b474c7638176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4093845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd9e1c4422d8331e63c2ab41ef04cf6709b4b7d584942e7bb2f133681a11589`

```dockerfile
```

-	Layers:
	-	`sha256:17468fd0050e3ed76e8779de813375c4e034301dc8d0f381e85854ed3468f74b`  
		Last Modified: Thu, 25 Jul 2024 19:29:58 GMT  
		Size: 4.1 MB (4057490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb48f7555b5da674117f7333e31c0565d4fa8efcb62b643f61e60457e8e6c617`  
		Last Modified: Thu, 25 Jul 2024 19:29:58 GMT  
		Size: 36.4 KB (36355 bytes)  
		MIME: application/vnd.in-toto+json
