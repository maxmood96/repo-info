## `solr:8-slim`

```console
$ docker pull solr@sha256:c207d5c965eb32bb7a12a731d757b8c3a70e2a90d15ddd9d0d05ee83fbf0b0a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `solr:8-slim` - linux; amd64

```console
$ docker pull solr@sha256:009a65653f4e994c51cb61429f664e2f5e9ed99cd0934de37622947a6ca2dcd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322391530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2761804501e43030c70ed2d3f0a3c05407ff6e0009543f81301e519dfa5cb2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=8.11.3
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512 # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=https://www.apache.org/dyn/closer.lua/lucene/solr/8.11.3/solr-8.11.3.tgz?action=download SOLR_DIST_URL=https://downloads.apache.org/lucene/solr/8.11.3/solr-8.11.3.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.3/solr-8.11.3.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0 # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY --chown=0:0 scripts /opt/docker-solr/scripts # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf168757422d85fc784edd9f8eab4082cd0da552a3faa4294d478d5faf0594d`  
		Last Modified: Tue, 16 Apr 2024 04:03:22 GMT  
		Size: 16.9 MB (16920620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a763dcd31ce3c009f23c280c3a52c469cd60e203be80de00afc5518523bec3c`  
		Last Modified: Tue, 16 Apr 2024 04:05:22 GMT  
		Size: 47.1 MB (47068135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2785594c667f0aefb6c072fe72d73dfa9dae97c9854d6e42ed9f85ff2185b3f`  
		Last Modified: Tue, 16 Apr 2024 04:05:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b793fdb5d3e7244d887b31b479788875238e1eaccf371c3260e358097728a31a`  
		Last Modified: Tue, 16 Apr 2024 04:05:16 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0986c3aeae80022cccd1634de3ce795d0ee8c3b99bb2aafa007a4ec9750be692`  
		Last Modified: Tue, 16 Apr 2024 05:57:27 GMT  
		Size: 4.7 MB (4663687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c44fbdfc33711a8984d420f449cdbfa9ec6baa17d4df510ce9e8f883deb6f75`  
		Last Modified: Tue, 16 Apr 2024 05:57:26 GMT  
		Size: 4.3 KB (4279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c002b15bfd30f971398a76add80e5fafed279b0df3b38c68387e18fd7263b9b`  
		Last Modified: Tue, 16 Apr 2024 05:57:27 GMT  
		Size: 2.9 KB (2891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da313cce28e7a220b892e09575911cb38a0892bb0ca3cbbc32048cb1aed44d46`  
		Last Modified: Tue, 16 Apr 2024 05:57:30 GMT  
		Size: 225.1 MB (225140217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300dc46e75ba9e6e359547c9cb4b21ec314e7f90a2b54eb13002fe7c10a951c7`  
		Last Modified: Tue, 16 Apr 2024 05:57:27 GMT  
		Size: 6.3 KB (6270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:e013db0ab3f14cddf9d6b1d01fb63f726f9dfd4c05022aa51dfdeb3fe05837f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4a0b9c09a4b34c729e45ec5c585bc8c842718b43cfd26a355e0a7c69f51e3e`

```dockerfile
```

-	Layers:
	-	`sha256:0cb76cd306a7ea54679dc2d869b0d8d813f65c89f04bbed6417498e25d1dac81`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 4.0 MB (3983798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9973acb16b930738f7bcfeb7c39bf51c303f9de01af6f9974992ae9ba2b5fc`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 37.1 KB (37112 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:9b596ab70d973b781fdebc53b1ea6725c62ea4cd6f742d6c211de6e4a8f5fa8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 MB (314589959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a195c8313bab65636657edacd6cf7a2a3c46f3b258c56021f412e04610ffcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:d5544f56cf9b2897ccff2833db59b6aa51af25a2aa34f4e000e12396d6b18f30 in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=8.11.3
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512 # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=https://www.apache.org/dyn/closer.lua/lucene/solr/8.11.3/solr-8.11.3.tgz?action=download SOLR_DIST_URL=https://downloads.apache.org/lucene/solr/8.11.3/solr-8.11.3.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.3/solr-8.11.3.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0 # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY --chown=0:0 scripts /opt/docker-solr/scripts # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:415e9bbd0769b29f08b5782353a86f2e8e29ba55d4d4d1e7fe999652679005c5`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 24.6 MB (24602624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d12b682cbcc5b59bbe1432d30883570b4dd781fd2260db8ec9fc50b11db15d2`  
		Last Modified: Tue, 16 Apr 2024 01:53:17 GMT  
		Size: 15.7 MB (15664712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a905ee9040660ed7f2b223af0a81915003ffdbe3abd6bb5d2564e15b58e187`  
		Last Modified: Tue, 16 Apr 2024 01:55:10 GMT  
		Size: 45.2 MB (45209681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190c64d0cfa2f7484eacf2ef7c39328e4e1f79c76824255b883f5d159de864fe`  
		Last Modified: Tue, 16 Apr 2024 01:55:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b007e8235a6acf00182927a09aabe1e8c2fb37715696cc7b8062ecccdd360391`  
		Last Modified: Tue, 16 Apr 2024 01:55:03 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecf5817dbaa2fbbf862c1182be6486c10d271892a55498d2a12e714a77bf5c9`  
		Last Modified: Tue, 16 Apr 2024 05:09:25 GMT  
		Size: 4.0 MB (3958086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771f29cfb9027bf8c20759524886816102a3d0a0e014d8a8df4679f34b31e80b`  
		Last Modified: Tue, 16 Apr 2024 05:09:24 GMT  
		Size: 4.2 KB (4202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d94116a5c8a3ca48984f82c028844c0d903da954827e8d6b2284fab56f06ab2`  
		Last Modified: Tue, 16 Apr 2024 05:09:24 GMT  
		Size: 2.9 KB (2888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c86e217e5c0a9b46afa1b1a944093599b141d4524dd923e098c87e4efe16c3d`  
		Last Modified: Tue, 16 Apr 2024 05:09:30 GMT  
		Size: 225.1 MB (225140569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ea616284361ac0cc8517e0bdcf1da1398c902975884be9e459f6a474f01664`  
		Last Modified: Tue, 16 Apr 2024 05:09:25 GMT  
		Size: 6.3 KB (6272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:f7d2099d0ba9176147fcc975cf0ca0263b7073d8a53ffc6ada14bab13980a63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4022482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffdf70bd3f2d2e892b797e681ac32d804c49297c590cb48e7790d4cfc72530b`

```dockerfile
```

-	Layers:
	-	`sha256:e996a06ce856ae9dbe22bc4b1f2f4bed93de7e7fd041031b74f8b95ab3bbc2b8`  
		Last Modified: Tue, 16 Apr 2024 05:09:49 GMT  
		Size: 4.0 MB (3986086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70555598288c36951e10e1d3e5f901f3c7d44cf52c2bf779a21b76eb84ddd14f`  
		Last Modified: Tue, 16 Apr 2024 05:09:49 GMT  
		Size: 36.4 KB (36396 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:5761c5f0075e2304cffb400beba4a8b546415f80507bb33dd098b6cdefcca8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319046169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d952f7cd795124588b9a585bf5b42704aba6ee62040cfd7ccb151adfc0a98d78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=8.11.3
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512 # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=https://www.apache.org/dyn/closer.lua/lucene/solr/8.11.3/solr-8.11.3.tgz?action=download SOLR_DIST_URL=https://downloads.apache.org/lucene/solr/8.11.3/solr-8.11.3.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.3/solr-8.11.3.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0 # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY scripts /opt/docker-solr/scripts # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:c2984f07e523b18eaa80a8ca4614feba1808673e5adbc26f162d2ee50031961c`  
		Last Modified: Sat, 17 Feb 2024 04:07:41 GMT  
		Size: 27.2 MB (27204287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bba6206cf5e5c72dd9d04c2269ff85b1ce7015a33a12585df751669013b790c`  
		Last Modified: Thu, 28 Mar 2024 00:48:26 GMT  
		Size: 16.8 MB (16776713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666babb87e1b877e1c99e4b7853c9bed35362d5c6682397f989071b16113bdf0`  
		Last Modified: Thu, 28 Mar 2024 00:51:36 GMT  
		Size: 45.4 MB (45398843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85558f92efd27f42214962f838718449db6c1a2993f56adc1bfed6295933daf`  
		Last Modified: Thu, 28 Mar 2024 00:51:30 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442ae6cc3a859547ae8fea84089d04cea00a5ea06c318dbe0027d22d39ce1317`  
		Last Modified: Thu, 28 Mar 2024 00:51:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5811684afd243ea7022d6c1712b818f884c6af32e1a6bc9c50fc4405379a54`  
		Last Modified: Thu, 28 Mar 2024 19:53:13 GMT  
		Size: 4.5 MB (4511673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee6fbdd884103753c411613db6109f70d03face801282c96b98fcfeb4065958`  
		Last Modified: Thu, 28 Mar 2024 19:53:13 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedc94aca768d5b5c4233244ef3cd56664dae45a3c0b5fdd998fc987892abde5`  
		Last Modified: Thu, 28 Mar 2024 19:53:14 GMT  
		Size: 2.9 KB (2887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f041c51df3aa67ce0f1c0dda51a1a3a961b51a7044cf356c02e792884eebda4`  
		Last Modified: Thu, 28 Mar 2024 19:53:19 GMT  
		Size: 225.1 MB (225140258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a806abcaba77ed3ea4619a0889aa65c25f51a20b9c05782110ee6cadda506e91`  
		Last Modified: Thu, 28 Mar 2024 19:53:14 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:f72cce509efd80f01a1c405072840f87fbb8c215fbf8bd57a5cd45545fe294ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4020332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86731d120c2346c055b9a3cd0668ca9386f9729184ab4ccebaa283b8e82bd9a2`

```dockerfile
```

-	Layers:
	-	`sha256:b446febc98f045c8eb0583e7783ef69c842cfcbb8a12ad3c8c1886a333af0f85`  
		Last Modified: Thu, 28 Mar 2024 19:53:37 GMT  
		Size: 4.0 MB (3984029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6555bc6f805a33dcecf0f2b87c46c36d2f16dc33cf10edee31da560d6d1385`  
		Last Modified: Thu, 28 Mar 2024 19:53:36 GMT  
		Size: 36.3 KB (36303 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:564f14e4b08efb18d61069c10cbc03c75787381e8079f39ea553f40da2953fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324729426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c6e87ad478a32c1841d12837980ec58fd1d3eb449e8946d80eaa33930d556c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:e8a9147477810033be455b6d05074e33f9e64458087ca10e58dbc087c80e00ad in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=8.11.3
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512 # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=https://www.apache.org/dyn/closer.lua/lucene/solr/8.11.3/solr-8.11.3.tgz?action=download SOLR_DIST_URL=https://downloads.apache.org/lucene/solr/8.11.3/solr-8.11.3.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.3/solr-8.11.3.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0 # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY scripts /opt/docker-solr/scripts # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:ecb7dea5440f763917c4b75b3f00c2617649ca914e65b3e965c37d6eb1e0dfde`  
		Last Modified: Wed, 06 Mar 2024 01:44:24 GMT  
		Size: 33.3 MB (33315609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cb7b12d05c6f7088aa73f03686c5693c7f8c0e33895a3df3b70702bc8d2037`  
		Last Modified: Thu, 28 Mar 2024 01:40:10 GMT  
		Size: 18.2 MB (18222011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99163e48c3a0e58e1ca664b14ec03f0c3df1f0b0cebede5f1c50e5f993a3e36`  
		Last Modified: Thu, 28 Mar 2024 01:44:09 GMT  
		Size: 42.5 MB (42497344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c89b94fb3ee876f07a6df013209d2cfdb279bde97a633c18ef99b765a81e6b6`  
		Last Modified: Thu, 28 Mar 2024 01:44:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34e032c319aaeccafeb63d8655f1972e9470c8cf7e7767f846813ceec13414`  
		Last Modified: Thu, 28 Mar 2024 01:44:02 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4ccbc1fa5185e42d6336bda7c5bda979c062bd0c4a330585dc16a972fe4573`  
		Last Modified: Thu, 28 Mar 2024 04:07:34 GMT  
		Size: 5.5 MB (5539697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240ec52d83154709329cb87af528f7e11b8de5f051305ff0d53e1ccc20e019df`  
		Last Modified: Thu, 28 Mar 2024 04:07:34 GMT  
		Size: 4.3 KB (4286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8a14c91d211581f3e51ecb427c214d5d7ca1196a6836470e7bf395709a821b`  
		Last Modified: Thu, 28 Mar 2024 04:07:35 GMT  
		Size: 2.9 KB (2890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a89c08c520fd9ef0072424e1daf0d5f667ad58e6971981b5282954fc9e21d71`  
		Last Modified: Thu, 28 Mar 2024 04:07:42 GMT  
		Size: 225.1 MB (225140388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0395a1f065364a7fd76769f6ced54e39fd003886a5bc9a1c1b236ec82c93689c`  
		Last Modified: Thu, 28 Mar 2024 04:07:35 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:baa3af14480e57297e20daac2bd0a9c819629dae2dfe105d1a3aa1bb33b67020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4024624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebb505b4d9870282d2d746950ec5b2ff987922d00878328212c9064c179de1c`

```dockerfile
```

-	Layers:
	-	`sha256:ca2ebc9b8d304a06268ec88825a9b7f2a516875ed402568fb5b0040ddc147b7a`  
		Last Modified: Thu, 28 Mar 2024 04:08:12 GMT  
		Size: 4.0 MB (3988291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:974b0cb5368278c4e37a8f98039d18a7847407f3d54a56d57c84900fd95bd112`  
		Last Modified: Thu, 28 Mar 2024 04:08:12 GMT  
		Size: 36.3 KB (36333 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:8-slim` - linux; s390x

```console
$ docker pull solr@sha256:20c96df5c43bdba2eeefc0df34e47734ab9a442bc55d51caa54446bc793df089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314075851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b08d1bab30ce7320660366eeec6df51eed3c77634388979a893780a5ed456b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:12253a4fd9294a85e33aaaf2aa2de64e7d8ff7b9a5ff1bef594e481337be991e in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='46e2bff7d5f419ac7c2fad29e78bfacf49ead4a2de1aba73b6329128f6d1f707';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='3a0fec1b9ef38d6abd86cf11f6001772b086096b6ec2588d2a02f1fa86b2b1de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='a5ab40aa53ecd413a8af738e66855d423e64b5389f876a4825e2cbdb45e9cfb3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='a6719f71217d0b6f931461acec465ca3a1eb0b0e94942fe165e27b30ecc341c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='1662e73deb814814fe27239666c5bf2d989484821343f0a3629ffb03729044ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jre_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=8.11.3
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512 # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=https://www.apache.org/dyn/closer.lua/lucene/solr/8.11.3/solr-8.11.3.tgz?action=download SOLR_DIST_URL=https://downloads.apache.org/lucene/solr/8.11.3/solr-8.11.3.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.3/solr-8.11.3.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0 # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=8.11.3 SOLR_SHA512=10f09b163bd9c31b2a8fdf889cf624114648e76881d69a4c096d473272c47b3cbe37ec9f9bd1980fd90967352c4052477065e165127eccb2c49a60c8d9860afc SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_URL= SOLR_DOWNLOAD_SERVER=
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY scripts /opt/docker-solr/scripts # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:9cc582e251a9a42e6189f6f7cbbf40c15a0588ecf0525cddc5871b0627cb34a8`  
		Last Modified: Wed, 06 Mar 2024 03:56:15 GMT  
		Size: 27.0 MB (27016065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc929bb9a6b27c14b0a1640566ace1efe6119961074f5ebfd01663248af09ab`  
		Last Modified: Thu, 28 Mar 2024 01:19:32 GMT  
		Size: 16.6 MB (16645739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cec4323689449d37b3d55a998e401435240d7e306219a68c8c4966ae42b5d1`  
		Last Modified: Thu, 28 Mar 2024 01:20:23 GMT  
		Size: 40.8 MB (40766110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03f92d302e97ba1cd114ddecbeeb939facddc45fcd62a04385cfe6c664ecfb8`  
		Last Modified: Thu, 28 Mar 2024 01:20:18 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650d5dcd477784ee1e5c3b92974147642b6be4eb894a82cc5250dcd809fc0d17`  
		Last Modified: Thu, 28 Mar 2024 01:20:18 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2c544ed9982724a2d909036accfd10fbf558f02cf206fcc1f8675151a483f1`  
		Last Modified: Thu, 28 Mar 2024 08:12:12 GMT  
		Size: 4.5 MB (4493272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07b9e79afb6eacff169a40f51249cc321bb99ede5ae8b8b6cb539c7e143cdcd`  
		Last Modified: Thu, 28 Mar 2024 08:12:13 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e2c9613077460edfdf5cda752f3cc7071b553baab1a801de13ab5350b1c889`  
		Last Modified: Thu, 28 Mar 2024 08:12:13 GMT  
		Size: 2.9 KB (2891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d6826ac61e390b048c9eae844096f136503130cb6b3dfc182def7939c33525`  
		Last Modified: Thu, 28 Mar 2024 08:12:17 GMT  
		Size: 225.1 MB (225140267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270236dcb695f2d87a1136e7f4b59c7dafeea6052929a87da6cef49542d35f9f`  
		Last Modified: Thu, 28 Mar 2024 08:12:13 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:8-slim` - unknown; unknown

```console
$ docker pull solr@sha256:3ccdac3ef75254269be5f86fb85c3b5f1280061105ff4fed7d1fdd05fbc23aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4021506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41df253b6992cca28f56c378dafb16bc2f7690401a1d1eb395653925d7b0bef`

```dockerfile
```

-	Layers:
	-	`sha256:717d8f74a4cf00a77059bdf22fffaa3dd5c896080bd55c29cd5af52fb4adedc5`  
		Last Modified: Thu, 28 Mar 2024 08:14:21 GMT  
		Size: 4.0 MB (3985211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b30380c7bd5cd74087de690104d5e6762ae983327652773256cdc09d5c8f0b9`  
		Last Modified: Thu, 28 Mar 2024 08:14:20 GMT  
		Size: 36.3 KB (36295 bytes)  
		MIME: application/vnd.in-toto+json
