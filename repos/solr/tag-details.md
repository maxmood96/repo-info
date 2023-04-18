<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `solr`

-	[`solr:8`](#solr8)
-	[`solr:8-slim`](#solr8-slim)
-	[`solr:8.11`](#solr811)
-	[`solr:8.11-slim`](#solr811-slim)
-	[`solr:8.11.2`](#solr8112)
-	[`solr:8.11.2-slim`](#solr8112-slim)
-	[`solr:9`](#solr9)
-	[`solr:9.0`](#solr90)
-	[`solr:9.0.0`](#solr900)
-	[`solr:9.1`](#solr91)
-	[`solr:9.1.1`](#solr911)
-	[`solr:9.2`](#solr92)
-	[`solr:9.2.0`](#solr920)
-	[`solr:latest`](#solrlatest)

## `solr:8`

```console
$ docker pull solr@sha256:213fd78add6f039335760ebdfaeb7843a01e7f3aa52a3350aff41e4a3e0521d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:8` - linux; amd64

```console
$ docker pull solr@sha256:b210a1886da5e6bd04b978e092ad2282fefb2b2ab9e928465b5c6d4cad58497d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314801289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fee171281dcf64fb86a69dad1e9390dee50678fea5dc79f0259935b9760cd04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 00:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 00:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 00:43:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:43:54 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 00:44:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 00:44:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 05:38:29 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 05:38:29 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 05:38:29 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 05:38:29 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 05:38:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 05:38:37 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 05:38:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 05:38:46 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 05:39:20 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 05:39:20 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 05:39:20 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 05:39:20 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 05:39:20 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 05:39:20 GMT
USER 8983
# Tue, 18 Apr 2023 05:39:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 05:39:21 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7affba4c9a33ed5dd050532c0d53e38b2c35c2fe490db721d943658feee4c914`  
		Last Modified: Tue, 18 Apr 2023 00:46:23 GMT  
		Size: 16.3 MB (16347011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fb5d08d03b0834295af88b5b911dca1240bcbdc3268dbc4c8ce24934ae017e`  
		Last Modified: Tue, 18 Apr 2023 00:47:26 GMT  
		Size: 46.6 MB (46632203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ef4a2443f5b89eae76a92c01bf3a006c986bb4fe658aa46a8dccc0bed2f523`  
		Last Modified: Tue, 18 Apr 2023 00:47:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e005372261eff41e611105a513fed9afaef08b30a879c639a8ac0efafd9300`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 4.9 MB (4901010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad0a251b15f3c813079323fdb45751b01c5753143b2c5dc1c6665bcc3e2680c`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 4.3 KB (4291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53da2eb3eae194651c65ebab849877740d6128968fd6e3f78f1a669b1ecb73d`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2462511e3bac8b859994f31534f2cfff6f8bfc787b5dc0909219b61ba839fdd1`  
		Last Modified: Tue, 18 Apr 2023 05:40:25 GMT  
		Size: 218.3 MB (218328276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7090d8a3f08936349556e936cfd4a9bfb2cd6661eeab03630417cee2cad95bfd`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 6.3 KB (6308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8` - linux; arm variant v7

```console
$ docker pull solr@sha256:b3c9697736d8208d626cff6651cc960c9311dd11f64a3eb1201af9d2d5b9ba63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307145944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1ab977a94d99fd58ad5909bb9e9369d6c96dbad9b2fce8b9a632c419774390`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:52:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:52:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:52:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:52:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:52:55 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:53:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:43:33 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 02:43:33 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:43:39 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 02:43:39 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 02:43:40 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:43:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 02:44:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 02:44:30 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 02:44:30 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:44:30 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:44:30 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:44:31 GMT
USER 8983
# Tue, 18 Apr 2023 02:44:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:44:31 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26020bb58aaff7bb6175448d285783e1d1698e726bcba90502c721abc88f2a2`  
		Last Modified: Tue, 18 Apr 2023 01:54:29 GMT  
		Size: 15.2 MB (15177669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07622852b9d8af8368242c298bb49668ea7975b2d9b6e4ac7c26bc7970508271`  
		Last Modified: Tue, 18 Apr 2023 01:55:29 GMT  
		Size: 44.8 MB (44843787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79339cee2747c7c082d0eaa5a711b4f5fd7a2875d6b6750d4bf589b282ae875`  
		Last Modified: Tue, 18 Apr 2023 01:55:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f70aeeae1860bbd48bdd953399d972be91807ea924ba06acdf3ba01345030`  
		Last Modified: Tue, 18 Apr 2023 02:45:34 GMT  
		Size: 4.2 MB (4195194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94952c7074a852730fda751b10e2166b7016df6315c67aedbdf50a8aab37d5ac`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 4.2 KB (4227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b56228b00077559f55a496496fc3498a3cd3387b66d45705967486a6283440`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a955106f4c93d7037f7715e10235bcccf43bdb83d6d00bd6e519230c2f0273c`  
		Last Modified: Tue, 18 Apr 2023 02:45:44 GMT  
		Size: 218.3 MB (218328154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0de5e28ecaf08af7bc911126dcbf7e95b93775829f90958146adab40f8b447`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:9c83437dd68f23bd3272fa16658b6bb0a96b4c47b0e19257d018071f1cbfe495
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311481859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0bcfc19e6f7e821e073ab8496a566a25ab40161cd530e90512c5f46ed1bf67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:40:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:40:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:41:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:41:31 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:41:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:41:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 03:21:22 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 03:21:23 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 03:21:28 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 03:21:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 03:21:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 03:21:43 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 03:22:14 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 03:22:16 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 03:22:16 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 03:22:16 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 03:22:16 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 03:22:16 GMT
USER 8983
# Tue, 18 Apr 2023 03:22:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 03:22:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269336393c4662b72ac4a2be29473801366e79f4db6c8b9944509f1903ee3fe6`  
		Last Modified: Tue, 18 Apr 2023 01:43:30 GMT  
		Size: 16.2 MB (16213349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775e69497bdf42d2ad7b39be6112c42f7fb711efa0036c55e9a5ddf8b30c244`  
		Last Modified: Tue, 18 Apr 2023 01:44:26 GMT  
		Size: 45.0 MB (44979459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff94c7a5594b10847f2895eb9f20938960ec3194f7398f5da8e801aff22ab00`  
		Last Modified: Tue, 18 Apr 2023 01:44:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3419bf7e5540a3bcd6132aa79f49429981574fb43627e2e617efd771123733e`  
		Last Modified: Tue, 18 Apr 2023 03:23:06 GMT  
		Size: 4.8 MB (4750130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f986cb8a544e5f5ed858bfd84e22a07cc5d8d5133bf126062e34097fb071cea9`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 4.3 KB (4335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46abce6c72ed3766b9f8dfbfadcecd21ca0597eef161bd3ef3b10408b72ae346`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbfb9f1a96f5d4bb8867ba070a31604ef992f2fe5672efd1775b3f3335be352`  
		Last Modified: Tue, 18 Apr 2023 03:23:15 GMT  
		Size: 218.3 MB (218328255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6099366efb07d013239cc98b209d1b555226441829877031336b84cc7f2f083`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 6.3 KB (6308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8` - linux; ppc64le

```console
$ docker pull solr@sha256:19c1b44a9bca9128a4069ed638cdcfc9c1798bba1421b33ab843e8f6e75096c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317067114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd4c81895762da00b4e9cd37462ffa750ebb80589f6511633158fd847760501`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:06:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:06:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:06:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:07:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:07:53 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:08:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:08:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:35:44 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 02:35:44 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 02:35:45 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 02:35:45 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 02:35:46 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 02:35:46 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:35:47 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:36:04 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 02:36:04 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 02:36:06 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:36:21 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 02:36:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 02:37:00 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 02:37:00 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:37:01 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:37:01 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:37:02 GMT
USER 8983
# Tue, 18 Apr 2023 02:37:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:37:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4018ee3c8b327c120bbf0427fb12e76c74cb054a92177aeeae16bcf0efa4e86`  
		Last Modified: Tue, 18 Apr 2023 01:11:24 GMT  
		Size: 17.6 MB (17582531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7790ee0621c15542c56b0e85f0263c81f9f6669f43fba1b253e99882262ffe6`  
		Last Modified: Tue, 18 Apr 2023 01:12:49 GMT  
		Size: 42.1 MB (42063861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41f4b7bd24a5b05c92949a1c05d6623acae52b5dfad264b0b2f5a039dd27309`  
		Last Modified: Tue, 18 Apr 2023 01:12:39 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15700e6ce1e1d806d636ec018e19719e2120a2c86c49fc3ea30b53bdd8cb4e53`  
		Last Modified: Tue, 18 Apr 2023 02:38:39 GMT  
		Size: 5.8 MB (5777224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1bdc6d63cfd771457f3b63241ca402866daafc083fa6a40856fa50462a5659`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86fa59a94ad403d12762e41a6b26d457d42e7e8b67d93566990919c5da301e`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecf09f805be54f9c957c79f858e1236520e512708a1e73ec27ab02efcb01494`  
		Last Modified: Tue, 18 Apr 2023 02:38:55 GMT  
		Size: 218.3 MB (218328288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7432224e033b9e67bcb4e97ac4c97c74022a8a9494d68f85c979018044e4a`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 6.3 KB (6306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8` - linux; s390x

```console
$ docker pull solr@sha256:389a866413fafae5f4a5524eadb24a3ffded326de4573a5a2ac7d590d86e76e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306661369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2623ddd1575fc5b45f9ddf500d45513829e78cd212412761a0a9945005a5b1ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:16:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:16:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:16:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:16:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:16:12 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:16:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:16:45 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 17:05:24 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 17:05:24 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 17:05:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 17:05:30 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 17:05:30 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 17:05:38 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 17:05:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 17:05:57 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 17:05:57 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 17:05:57 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 17:05:57 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 17:05:57 GMT
USER 8983
# Tue, 18 Apr 2023 17:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 17:05:57 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c307a57c5f07334cfab6db8f8324b0c9dff13121ec34d8db1d4a71e3529d4b5`  
		Last Modified: Tue, 18 Apr 2023 01:18:27 GMT  
		Size: 16.0 MB (16035272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edda216cc8ab33b8b4e53985609e8e8a98a3d295b6519ae9cb4f56fddbc35b6`  
		Last Modified: Tue, 18 Apr 2023 01:18:51 GMT  
		Size: 40.5 MB (40536784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bc476f2e4aba994464557beb4b38f1f1e73bf5cd02747e0f5c064af9c09bcc`  
		Last Modified: Tue, 18 Apr 2023 01:18:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7669fc3a7d75e3555f6ba98cd20d1ca196363ff6bad746e5027a023dc3dafe6f`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 4.7 MB (4730499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8708d9d2106caa9217180b74c334f5e6061dfa508e5f1612f4735fb8733b93f7`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a7defad728ae326c204388e49119c44a9cece1aad251d3224fed0f20fe9778`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 3.5 KB (3468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aebbf0c5137798a5b604fcd11bff32a718321a9ced08624b590f3b924ae29a0`  
		Last Modified: Tue, 18 Apr 2023 17:07:07 GMT  
		Size: 218.3 MB (218328179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bd21199ecdc92fc3907f7629a84a36f1a759a2855a8a4831c518182a02d91c`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 6.3 KB (6306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:8-slim`

```console
$ docker pull solr@sha256:213fd78add6f039335760ebdfaeb7843a01e7f3aa52a3350aff41e4a3e0521d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:8-slim` - linux; amd64

```console
$ docker pull solr@sha256:b210a1886da5e6bd04b978e092ad2282fefb2b2ab9e928465b5c6d4cad58497d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314801289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fee171281dcf64fb86a69dad1e9390dee50678fea5dc79f0259935b9760cd04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 00:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 00:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 00:43:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:43:54 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 00:44:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 00:44:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 05:38:29 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 05:38:29 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 05:38:29 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 05:38:29 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 05:38:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 05:38:37 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 05:38:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 05:38:46 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 05:39:20 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 05:39:20 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 05:39:20 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 05:39:20 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 05:39:20 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 05:39:20 GMT
USER 8983
# Tue, 18 Apr 2023 05:39:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 05:39:21 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7affba4c9a33ed5dd050532c0d53e38b2c35c2fe490db721d943658feee4c914`  
		Last Modified: Tue, 18 Apr 2023 00:46:23 GMT  
		Size: 16.3 MB (16347011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fb5d08d03b0834295af88b5b911dca1240bcbdc3268dbc4c8ce24934ae017e`  
		Last Modified: Tue, 18 Apr 2023 00:47:26 GMT  
		Size: 46.6 MB (46632203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ef4a2443f5b89eae76a92c01bf3a006c986bb4fe658aa46a8dccc0bed2f523`  
		Last Modified: Tue, 18 Apr 2023 00:47:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e005372261eff41e611105a513fed9afaef08b30a879c639a8ac0efafd9300`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 4.9 MB (4901010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad0a251b15f3c813079323fdb45751b01c5753143b2c5dc1c6665bcc3e2680c`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 4.3 KB (4291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53da2eb3eae194651c65ebab849877740d6128968fd6e3f78f1a669b1ecb73d`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2462511e3bac8b859994f31534f2cfff6f8bfc787b5dc0909219b61ba839fdd1`  
		Last Modified: Tue, 18 Apr 2023 05:40:25 GMT  
		Size: 218.3 MB (218328276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7090d8a3f08936349556e936cfd4a9bfb2cd6661eeab03630417cee2cad95bfd`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 6.3 KB (6308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:b3c9697736d8208d626cff6651cc960c9311dd11f64a3eb1201af9d2d5b9ba63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307145944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1ab977a94d99fd58ad5909bb9e9369d6c96dbad9b2fce8b9a632c419774390`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:52:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:52:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:52:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:52:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:52:55 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:53:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:43:33 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 02:43:33 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:43:39 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 02:43:39 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 02:43:40 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:43:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 02:44:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 02:44:30 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 02:44:30 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:44:30 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:44:30 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:44:31 GMT
USER 8983
# Tue, 18 Apr 2023 02:44:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:44:31 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26020bb58aaff7bb6175448d285783e1d1698e726bcba90502c721abc88f2a2`  
		Last Modified: Tue, 18 Apr 2023 01:54:29 GMT  
		Size: 15.2 MB (15177669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07622852b9d8af8368242c298bb49668ea7975b2d9b6e4ac7c26bc7970508271`  
		Last Modified: Tue, 18 Apr 2023 01:55:29 GMT  
		Size: 44.8 MB (44843787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79339cee2747c7c082d0eaa5a711b4f5fd7a2875d6b6750d4bf589b282ae875`  
		Last Modified: Tue, 18 Apr 2023 01:55:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f70aeeae1860bbd48bdd953399d972be91807ea924ba06acdf3ba01345030`  
		Last Modified: Tue, 18 Apr 2023 02:45:34 GMT  
		Size: 4.2 MB (4195194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94952c7074a852730fda751b10e2166b7016df6315c67aedbdf50a8aab37d5ac`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 4.2 KB (4227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b56228b00077559f55a496496fc3498a3cd3387b66d45705967486a6283440`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a955106f4c93d7037f7715e10235bcccf43bdb83d6d00bd6e519230c2f0273c`  
		Last Modified: Tue, 18 Apr 2023 02:45:44 GMT  
		Size: 218.3 MB (218328154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0de5e28ecaf08af7bc911126dcbf7e95b93775829f90958146adab40f8b447`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:9c83437dd68f23bd3272fa16658b6bb0a96b4c47b0e19257d018071f1cbfe495
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311481859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0bcfc19e6f7e821e073ab8496a566a25ab40161cd530e90512c5f46ed1bf67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:40:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:40:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:41:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:41:31 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:41:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:41:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 03:21:22 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 03:21:23 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 03:21:28 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 03:21:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 03:21:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 03:21:43 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 03:22:14 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 03:22:16 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 03:22:16 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 03:22:16 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 03:22:16 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 03:22:16 GMT
USER 8983
# Tue, 18 Apr 2023 03:22:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 03:22:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269336393c4662b72ac4a2be29473801366e79f4db6c8b9944509f1903ee3fe6`  
		Last Modified: Tue, 18 Apr 2023 01:43:30 GMT  
		Size: 16.2 MB (16213349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775e69497bdf42d2ad7b39be6112c42f7fb711efa0036c55e9a5ddf8b30c244`  
		Last Modified: Tue, 18 Apr 2023 01:44:26 GMT  
		Size: 45.0 MB (44979459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff94c7a5594b10847f2895eb9f20938960ec3194f7398f5da8e801aff22ab00`  
		Last Modified: Tue, 18 Apr 2023 01:44:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3419bf7e5540a3bcd6132aa79f49429981574fb43627e2e617efd771123733e`  
		Last Modified: Tue, 18 Apr 2023 03:23:06 GMT  
		Size: 4.8 MB (4750130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f986cb8a544e5f5ed858bfd84e22a07cc5d8d5133bf126062e34097fb071cea9`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 4.3 KB (4335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46abce6c72ed3766b9f8dfbfadcecd21ca0597eef161bd3ef3b10408b72ae346`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbfb9f1a96f5d4bb8867ba070a31604ef992f2fe5672efd1775b3f3335be352`  
		Last Modified: Tue, 18 Apr 2023 03:23:15 GMT  
		Size: 218.3 MB (218328255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6099366efb07d013239cc98b209d1b555226441829877031336b84cc7f2f083`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 6.3 KB (6308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:19c1b44a9bca9128a4069ed638cdcfc9c1798bba1421b33ab843e8f6e75096c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317067114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd4c81895762da00b4e9cd37462ffa750ebb80589f6511633158fd847760501`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:06:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:06:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:06:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:07:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:07:53 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:08:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:08:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:35:44 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 02:35:44 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 02:35:45 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 02:35:45 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 02:35:46 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 02:35:46 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:35:47 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:36:04 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 02:36:04 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 02:36:06 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:36:21 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 02:36:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 02:37:00 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 02:37:00 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:37:01 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:37:01 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:37:02 GMT
USER 8983
# Tue, 18 Apr 2023 02:37:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:37:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4018ee3c8b327c120bbf0427fb12e76c74cb054a92177aeeae16bcf0efa4e86`  
		Last Modified: Tue, 18 Apr 2023 01:11:24 GMT  
		Size: 17.6 MB (17582531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7790ee0621c15542c56b0e85f0263c81f9f6669f43fba1b253e99882262ffe6`  
		Last Modified: Tue, 18 Apr 2023 01:12:49 GMT  
		Size: 42.1 MB (42063861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41f4b7bd24a5b05c92949a1c05d6623acae52b5dfad264b0b2f5a039dd27309`  
		Last Modified: Tue, 18 Apr 2023 01:12:39 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15700e6ce1e1d806d636ec018e19719e2120a2c86c49fc3ea30b53bdd8cb4e53`  
		Last Modified: Tue, 18 Apr 2023 02:38:39 GMT  
		Size: 5.8 MB (5777224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1bdc6d63cfd771457f3b63241ca402866daafc083fa6a40856fa50462a5659`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86fa59a94ad403d12762e41a6b26d457d42e7e8b67d93566990919c5da301e`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecf09f805be54f9c957c79f858e1236520e512708a1e73ec27ab02efcb01494`  
		Last Modified: Tue, 18 Apr 2023 02:38:55 GMT  
		Size: 218.3 MB (218328288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7432224e033b9e67bcb4e97ac4c97c74022a8a9494d68f85c979018044e4a`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 6.3 KB (6306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; s390x

```console
$ docker pull solr@sha256:389a866413fafae5f4a5524eadb24a3ffded326de4573a5a2ac7d590d86e76e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306661369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2623ddd1575fc5b45f9ddf500d45513829e78cd212412761a0a9945005a5b1ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:16:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:16:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:16:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:16:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:16:12 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:16:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:16:45 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 17:05:24 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 17:05:24 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 17:05:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 17:05:30 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 17:05:30 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 17:05:38 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 17:05:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 17:05:57 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 17:05:57 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 17:05:57 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 17:05:57 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 17:05:57 GMT
USER 8983
# Tue, 18 Apr 2023 17:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 17:05:57 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c307a57c5f07334cfab6db8f8324b0c9dff13121ec34d8db1d4a71e3529d4b5`  
		Last Modified: Tue, 18 Apr 2023 01:18:27 GMT  
		Size: 16.0 MB (16035272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edda216cc8ab33b8b4e53985609e8e8a98a3d295b6519ae9cb4f56fddbc35b6`  
		Last Modified: Tue, 18 Apr 2023 01:18:51 GMT  
		Size: 40.5 MB (40536784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bc476f2e4aba994464557beb4b38f1f1e73bf5cd02747e0f5c064af9c09bcc`  
		Last Modified: Tue, 18 Apr 2023 01:18:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7669fc3a7d75e3555f6ba98cd20d1ca196363ff6bad746e5027a023dc3dafe6f`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 4.7 MB (4730499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8708d9d2106caa9217180b74c334f5e6061dfa508e5f1612f4735fb8733b93f7`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a7defad728ae326c204388e49119c44a9cece1aad251d3224fed0f20fe9778`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 3.5 KB (3468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aebbf0c5137798a5b604fcd11bff32a718321a9ced08624b590f3b924ae29a0`  
		Last Modified: Tue, 18 Apr 2023 17:07:07 GMT  
		Size: 218.3 MB (218328179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bd21199ecdc92fc3907f7629a84a36f1a759a2855a8a4831c518182a02d91c`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 6.3 KB (6306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:8.11`

```console
$ docker pull solr@sha256:213fd78add6f039335760ebdfaeb7843a01e7f3aa52a3350aff41e4a3e0521d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:8.11` - linux; amd64

```console
$ docker pull solr@sha256:b210a1886da5e6bd04b978e092ad2282fefb2b2ab9e928465b5c6d4cad58497d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314801289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fee171281dcf64fb86a69dad1e9390dee50678fea5dc79f0259935b9760cd04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 00:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 00:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 00:43:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:43:54 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 00:44:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 00:44:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 05:38:29 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 05:38:29 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 05:38:29 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 05:38:29 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 05:38:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 05:38:37 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 05:38:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 05:38:46 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 05:39:20 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 05:39:20 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 05:39:20 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 05:39:20 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 05:39:20 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 05:39:20 GMT
USER 8983
# Tue, 18 Apr 2023 05:39:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 05:39:21 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7affba4c9a33ed5dd050532c0d53e38b2c35c2fe490db721d943658feee4c914`  
		Last Modified: Tue, 18 Apr 2023 00:46:23 GMT  
		Size: 16.3 MB (16347011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fb5d08d03b0834295af88b5b911dca1240bcbdc3268dbc4c8ce24934ae017e`  
		Last Modified: Tue, 18 Apr 2023 00:47:26 GMT  
		Size: 46.6 MB (46632203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ef4a2443f5b89eae76a92c01bf3a006c986bb4fe658aa46a8dccc0bed2f523`  
		Last Modified: Tue, 18 Apr 2023 00:47:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e005372261eff41e611105a513fed9afaef08b30a879c639a8ac0efafd9300`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 4.9 MB (4901010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad0a251b15f3c813079323fdb45751b01c5753143b2c5dc1c6665bcc3e2680c`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 4.3 KB (4291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53da2eb3eae194651c65ebab849877740d6128968fd6e3f78f1a669b1ecb73d`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2462511e3bac8b859994f31534f2cfff6f8bfc787b5dc0909219b61ba839fdd1`  
		Last Modified: Tue, 18 Apr 2023 05:40:25 GMT  
		Size: 218.3 MB (218328276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7090d8a3f08936349556e936cfd4a9bfb2cd6661eeab03630417cee2cad95bfd`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 6.3 KB (6308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11` - linux; arm variant v7

```console
$ docker pull solr@sha256:b3c9697736d8208d626cff6651cc960c9311dd11f64a3eb1201af9d2d5b9ba63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307145944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1ab977a94d99fd58ad5909bb9e9369d6c96dbad9b2fce8b9a632c419774390`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:52:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:52:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:52:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:52:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:52:55 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:53:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:43:33 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 02:43:33 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:43:39 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 02:43:39 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 02:43:40 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:43:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 02:44:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 02:44:30 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 02:44:30 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:44:30 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:44:30 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:44:31 GMT
USER 8983
# Tue, 18 Apr 2023 02:44:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:44:31 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26020bb58aaff7bb6175448d285783e1d1698e726bcba90502c721abc88f2a2`  
		Last Modified: Tue, 18 Apr 2023 01:54:29 GMT  
		Size: 15.2 MB (15177669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07622852b9d8af8368242c298bb49668ea7975b2d9b6e4ac7c26bc7970508271`  
		Last Modified: Tue, 18 Apr 2023 01:55:29 GMT  
		Size: 44.8 MB (44843787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79339cee2747c7c082d0eaa5a711b4f5fd7a2875d6b6750d4bf589b282ae875`  
		Last Modified: Tue, 18 Apr 2023 01:55:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f70aeeae1860bbd48bdd953399d972be91807ea924ba06acdf3ba01345030`  
		Last Modified: Tue, 18 Apr 2023 02:45:34 GMT  
		Size: 4.2 MB (4195194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94952c7074a852730fda751b10e2166b7016df6315c67aedbdf50a8aab37d5ac`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 4.2 KB (4227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b56228b00077559f55a496496fc3498a3cd3387b66d45705967486a6283440`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a955106f4c93d7037f7715e10235bcccf43bdb83d6d00bd6e519230c2f0273c`  
		Last Modified: Tue, 18 Apr 2023 02:45:44 GMT  
		Size: 218.3 MB (218328154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0de5e28ecaf08af7bc911126dcbf7e95b93775829f90958146adab40f8b447`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:9c83437dd68f23bd3272fa16658b6bb0a96b4c47b0e19257d018071f1cbfe495
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311481859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0bcfc19e6f7e821e073ab8496a566a25ab40161cd530e90512c5f46ed1bf67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:40:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:40:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:41:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:41:31 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:41:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:41:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 03:21:22 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 03:21:23 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 03:21:28 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 03:21:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 03:21:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 03:21:43 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 03:22:14 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 03:22:16 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 03:22:16 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 03:22:16 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 03:22:16 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 03:22:16 GMT
USER 8983
# Tue, 18 Apr 2023 03:22:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 03:22:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269336393c4662b72ac4a2be29473801366e79f4db6c8b9944509f1903ee3fe6`  
		Last Modified: Tue, 18 Apr 2023 01:43:30 GMT  
		Size: 16.2 MB (16213349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775e69497bdf42d2ad7b39be6112c42f7fb711efa0036c55e9a5ddf8b30c244`  
		Last Modified: Tue, 18 Apr 2023 01:44:26 GMT  
		Size: 45.0 MB (44979459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff94c7a5594b10847f2895eb9f20938960ec3194f7398f5da8e801aff22ab00`  
		Last Modified: Tue, 18 Apr 2023 01:44:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3419bf7e5540a3bcd6132aa79f49429981574fb43627e2e617efd771123733e`  
		Last Modified: Tue, 18 Apr 2023 03:23:06 GMT  
		Size: 4.8 MB (4750130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f986cb8a544e5f5ed858bfd84e22a07cc5d8d5133bf126062e34097fb071cea9`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 4.3 KB (4335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46abce6c72ed3766b9f8dfbfadcecd21ca0597eef161bd3ef3b10408b72ae346`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbfb9f1a96f5d4bb8867ba070a31604ef992f2fe5672efd1775b3f3335be352`  
		Last Modified: Tue, 18 Apr 2023 03:23:15 GMT  
		Size: 218.3 MB (218328255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6099366efb07d013239cc98b209d1b555226441829877031336b84cc7f2f083`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 6.3 KB (6308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11` - linux; ppc64le

```console
$ docker pull solr@sha256:19c1b44a9bca9128a4069ed638cdcfc9c1798bba1421b33ab843e8f6e75096c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317067114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd4c81895762da00b4e9cd37462ffa750ebb80589f6511633158fd847760501`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:06:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:06:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:06:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:07:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:07:53 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:08:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:08:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:35:44 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 02:35:44 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 02:35:45 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 02:35:45 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 02:35:46 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 02:35:46 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:35:47 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:36:04 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 02:36:04 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 02:36:06 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:36:21 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 02:36:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 02:37:00 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 02:37:00 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:37:01 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:37:01 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:37:02 GMT
USER 8983
# Tue, 18 Apr 2023 02:37:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:37:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4018ee3c8b327c120bbf0427fb12e76c74cb054a92177aeeae16bcf0efa4e86`  
		Last Modified: Tue, 18 Apr 2023 01:11:24 GMT  
		Size: 17.6 MB (17582531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7790ee0621c15542c56b0e85f0263c81f9f6669f43fba1b253e99882262ffe6`  
		Last Modified: Tue, 18 Apr 2023 01:12:49 GMT  
		Size: 42.1 MB (42063861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41f4b7bd24a5b05c92949a1c05d6623acae52b5dfad264b0b2f5a039dd27309`  
		Last Modified: Tue, 18 Apr 2023 01:12:39 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15700e6ce1e1d806d636ec018e19719e2120a2c86c49fc3ea30b53bdd8cb4e53`  
		Last Modified: Tue, 18 Apr 2023 02:38:39 GMT  
		Size: 5.8 MB (5777224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1bdc6d63cfd771457f3b63241ca402866daafc083fa6a40856fa50462a5659`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86fa59a94ad403d12762e41a6b26d457d42e7e8b67d93566990919c5da301e`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecf09f805be54f9c957c79f858e1236520e512708a1e73ec27ab02efcb01494`  
		Last Modified: Tue, 18 Apr 2023 02:38:55 GMT  
		Size: 218.3 MB (218328288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7432224e033b9e67bcb4e97ac4c97c74022a8a9494d68f85c979018044e4a`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 6.3 KB (6306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11` - linux; s390x

```console
$ docker pull solr@sha256:389a866413fafae5f4a5524eadb24a3ffded326de4573a5a2ac7d590d86e76e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306661369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2623ddd1575fc5b45f9ddf500d45513829e78cd212412761a0a9945005a5b1ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:16:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:16:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:16:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:16:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:16:12 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:16:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:16:45 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 17:05:24 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 17:05:24 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 17:05:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 17:05:30 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 17:05:30 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 17:05:38 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 17:05:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 17:05:57 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 17:05:57 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 17:05:57 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 17:05:57 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 17:05:57 GMT
USER 8983
# Tue, 18 Apr 2023 17:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 17:05:57 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c307a57c5f07334cfab6db8f8324b0c9dff13121ec34d8db1d4a71e3529d4b5`  
		Last Modified: Tue, 18 Apr 2023 01:18:27 GMT  
		Size: 16.0 MB (16035272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edda216cc8ab33b8b4e53985609e8e8a98a3d295b6519ae9cb4f56fddbc35b6`  
		Last Modified: Tue, 18 Apr 2023 01:18:51 GMT  
		Size: 40.5 MB (40536784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bc476f2e4aba994464557beb4b38f1f1e73bf5cd02747e0f5c064af9c09bcc`  
		Last Modified: Tue, 18 Apr 2023 01:18:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7669fc3a7d75e3555f6ba98cd20d1ca196363ff6bad746e5027a023dc3dafe6f`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 4.7 MB (4730499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8708d9d2106caa9217180b74c334f5e6061dfa508e5f1612f4735fb8733b93f7`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a7defad728ae326c204388e49119c44a9cece1aad251d3224fed0f20fe9778`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 3.5 KB (3468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aebbf0c5137798a5b604fcd11bff32a718321a9ced08624b590f3b924ae29a0`  
		Last Modified: Tue, 18 Apr 2023 17:07:07 GMT  
		Size: 218.3 MB (218328179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bd21199ecdc92fc3907f7629a84a36f1a759a2855a8a4831c518182a02d91c`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 6.3 KB (6306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:8.11-slim`

```console
$ docker pull solr@sha256:213fd78add6f039335760ebdfaeb7843a01e7f3aa52a3350aff41e4a3e0521d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:8.11-slim` - linux; amd64

```console
$ docker pull solr@sha256:b210a1886da5e6bd04b978e092ad2282fefb2b2ab9e928465b5c6d4cad58497d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314801289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fee171281dcf64fb86a69dad1e9390dee50678fea5dc79f0259935b9760cd04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 00:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 00:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 00:43:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:43:54 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 00:44:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 00:44:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 05:38:29 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 05:38:29 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 05:38:29 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 05:38:29 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 05:38:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 05:38:37 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 05:38:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 05:38:46 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 05:39:20 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 05:39:20 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 05:39:20 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 05:39:20 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 05:39:20 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 05:39:20 GMT
USER 8983
# Tue, 18 Apr 2023 05:39:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 05:39:21 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7affba4c9a33ed5dd050532c0d53e38b2c35c2fe490db721d943658feee4c914`  
		Last Modified: Tue, 18 Apr 2023 00:46:23 GMT  
		Size: 16.3 MB (16347011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fb5d08d03b0834295af88b5b911dca1240bcbdc3268dbc4c8ce24934ae017e`  
		Last Modified: Tue, 18 Apr 2023 00:47:26 GMT  
		Size: 46.6 MB (46632203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ef4a2443f5b89eae76a92c01bf3a006c986bb4fe658aa46a8dccc0bed2f523`  
		Last Modified: Tue, 18 Apr 2023 00:47:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e005372261eff41e611105a513fed9afaef08b30a879c639a8ac0efafd9300`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 4.9 MB (4901010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad0a251b15f3c813079323fdb45751b01c5753143b2c5dc1c6665bcc3e2680c`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 4.3 KB (4291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53da2eb3eae194651c65ebab849877740d6128968fd6e3f78f1a669b1ecb73d`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2462511e3bac8b859994f31534f2cfff6f8bfc787b5dc0909219b61ba839fdd1`  
		Last Modified: Tue, 18 Apr 2023 05:40:25 GMT  
		Size: 218.3 MB (218328276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7090d8a3f08936349556e936cfd4a9bfb2cd6661eeab03630417cee2cad95bfd`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 6.3 KB (6308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11-slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:b3c9697736d8208d626cff6651cc960c9311dd11f64a3eb1201af9d2d5b9ba63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307145944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1ab977a94d99fd58ad5909bb9e9369d6c96dbad9b2fce8b9a632c419774390`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:52:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:52:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:52:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:52:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:52:55 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:53:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:43:33 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 02:43:33 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:43:39 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 02:43:39 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 02:43:40 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:43:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 02:44:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 02:44:30 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 02:44:30 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:44:30 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:44:30 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:44:31 GMT
USER 8983
# Tue, 18 Apr 2023 02:44:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:44:31 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26020bb58aaff7bb6175448d285783e1d1698e726bcba90502c721abc88f2a2`  
		Last Modified: Tue, 18 Apr 2023 01:54:29 GMT  
		Size: 15.2 MB (15177669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07622852b9d8af8368242c298bb49668ea7975b2d9b6e4ac7c26bc7970508271`  
		Last Modified: Tue, 18 Apr 2023 01:55:29 GMT  
		Size: 44.8 MB (44843787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79339cee2747c7c082d0eaa5a711b4f5fd7a2875d6b6750d4bf589b282ae875`  
		Last Modified: Tue, 18 Apr 2023 01:55:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f70aeeae1860bbd48bdd953399d972be91807ea924ba06acdf3ba01345030`  
		Last Modified: Tue, 18 Apr 2023 02:45:34 GMT  
		Size: 4.2 MB (4195194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94952c7074a852730fda751b10e2166b7016df6315c67aedbdf50a8aab37d5ac`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 4.2 KB (4227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b56228b00077559f55a496496fc3498a3cd3387b66d45705967486a6283440`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a955106f4c93d7037f7715e10235bcccf43bdb83d6d00bd6e519230c2f0273c`  
		Last Modified: Tue, 18 Apr 2023 02:45:44 GMT  
		Size: 218.3 MB (218328154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0de5e28ecaf08af7bc911126dcbf7e95b93775829f90958146adab40f8b447`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:9c83437dd68f23bd3272fa16658b6bb0a96b4c47b0e19257d018071f1cbfe495
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311481859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0bcfc19e6f7e821e073ab8496a566a25ab40161cd530e90512c5f46ed1bf67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:40:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:40:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:41:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:41:31 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:41:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:41:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 03:21:22 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 03:21:23 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 03:21:28 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 03:21:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 03:21:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 03:21:43 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 03:22:14 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 03:22:16 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 03:22:16 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 03:22:16 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 03:22:16 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 03:22:16 GMT
USER 8983
# Tue, 18 Apr 2023 03:22:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 03:22:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269336393c4662b72ac4a2be29473801366e79f4db6c8b9944509f1903ee3fe6`  
		Last Modified: Tue, 18 Apr 2023 01:43:30 GMT  
		Size: 16.2 MB (16213349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775e69497bdf42d2ad7b39be6112c42f7fb711efa0036c55e9a5ddf8b30c244`  
		Last Modified: Tue, 18 Apr 2023 01:44:26 GMT  
		Size: 45.0 MB (44979459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff94c7a5594b10847f2895eb9f20938960ec3194f7398f5da8e801aff22ab00`  
		Last Modified: Tue, 18 Apr 2023 01:44:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3419bf7e5540a3bcd6132aa79f49429981574fb43627e2e617efd771123733e`  
		Last Modified: Tue, 18 Apr 2023 03:23:06 GMT  
		Size: 4.8 MB (4750130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f986cb8a544e5f5ed858bfd84e22a07cc5d8d5133bf126062e34097fb071cea9`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 4.3 KB (4335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46abce6c72ed3766b9f8dfbfadcecd21ca0597eef161bd3ef3b10408b72ae346`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbfb9f1a96f5d4bb8867ba070a31604ef992f2fe5672efd1775b3f3335be352`  
		Last Modified: Tue, 18 Apr 2023 03:23:15 GMT  
		Size: 218.3 MB (218328255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6099366efb07d013239cc98b209d1b555226441829877031336b84cc7f2f083`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 6.3 KB (6308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:19c1b44a9bca9128a4069ed638cdcfc9c1798bba1421b33ab843e8f6e75096c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317067114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd4c81895762da00b4e9cd37462ffa750ebb80589f6511633158fd847760501`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:06:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:06:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:06:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:07:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:07:53 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:08:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:08:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:35:44 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 02:35:44 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 02:35:45 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 02:35:45 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 02:35:46 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 02:35:46 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:35:47 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:36:04 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 02:36:04 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 02:36:06 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:36:21 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 02:36:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 02:37:00 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 02:37:00 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:37:01 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:37:01 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:37:02 GMT
USER 8983
# Tue, 18 Apr 2023 02:37:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:37:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4018ee3c8b327c120bbf0427fb12e76c74cb054a92177aeeae16bcf0efa4e86`  
		Last Modified: Tue, 18 Apr 2023 01:11:24 GMT  
		Size: 17.6 MB (17582531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7790ee0621c15542c56b0e85f0263c81f9f6669f43fba1b253e99882262ffe6`  
		Last Modified: Tue, 18 Apr 2023 01:12:49 GMT  
		Size: 42.1 MB (42063861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41f4b7bd24a5b05c92949a1c05d6623acae52b5dfad264b0b2f5a039dd27309`  
		Last Modified: Tue, 18 Apr 2023 01:12:39 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15700e6ce1e1d806d636ec018e19719e2120a2c86c49fc3ea30b53bdd8cb4e53`  
		Last Modified: Tue, 18 Apr 2023 02:38:39 GMT  
		Size: 5.8 MB (5777224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1bdc6d63cfd771457f3b63241ca402866daafc083fa6a40856fa50462a5659`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86fa59a94ad403d12762e41a6b26d457d42e7e8b67d93566990919c5da301e`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecf09f805be54f9c957c79f858e1236520e512708a1e73ec27ab02efcb01494`  
		Last Modified: Tue, 18 Apr 2023 02:38:55 GMT  
		Size: 218.3 MB (218328288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7432224e033b9e67bcb4e97ac4c97c74022a8a9494d68f85c979018044e4a`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 6.3 KB (6306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11-slim` - linux; s390x

```console
$ docker pull solr@sha256:389a866413fafae5f4a5524eadb24a3ffded326de4573a5a2ac7d590d86e76e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306661369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2623ddd1575fc5b45f9ddf500d45513829e78cd212412761a0a9945005a5b1ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:16:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:16:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:16:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:16:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:16:12 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:16:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:16:45 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 17:05:24 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 17:05:24 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 17:05:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 17:05:30 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 17:05:30 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 17:05:38 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 17:05:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 17:05:57 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 17:05:57 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 17:05:57 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 17:05:57 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 17:05:57 GMT
USER 8983
# Tue, 18 Apr 2023 17:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 17:05:57 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c307a57c5f07334cfab6db8f8324b0c9dff13121ec34d8db1d4a71e3529d4b5`  
		Last Modified: Tue, 18 Apr 2023 01:18:27 GMT  
		Size: 16.0 MB (16035272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edda216cc8ab33b8b4e53985609e8e8a98a3d295b6519ae9cb4f56fddbc35b6`  
		Last Modified: Tue, 18 Apr 2023 01:18:51 GMT  
		Size: 40.5 MB (40536784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bc476f2e4aba994464557beb4b38f1f1e73bf5cd02747e0f5c064af9c09bcc`  
		Last Modified: Tue, 18 Apr 2023 01:18:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7669fc3a7d75e3555f6ba98cd20d1ca196363ff6bad746e5027a023dc3dafe6f`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 4.7 MB (4730499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8708d9d2106caa9217180b74c334f5e6061dfa508e5f1612f4735fb8733b93f7`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a7defad728ae326c204388e49119c44a9cece1aad251d3224fed0f20fe9778`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 3.5 KB (3468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aebbf0c5137798a5b604fcd11bff32a718321a9ced08624b590f3b924ae29a0`  
		Last Modified: Tue, 18 Apr 2023 17:07:07 GMT  
		Size: 218.3 MB (218328179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bd21199ecdc92fc3907f7629a84a36f1a759a2855a8a4831c518182a02d91c`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 6.3 KB (6306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:8.11.2`

```console
$ docker pull solr@sha256:213fd78add6f039335760ebdfaeb7843a01e7f3aa52a3350aff41e4a3e0521d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:8.11.2` - linux; amd64

```console
$ docker pull solr@sha256:b210a1886da5e6bd04b978e092ad2282fefb2b2ab9e928465b5c6d4cad58497d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314801289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fee171281dcf64fb86a69dad1e9390dee50678fea5dc79f0259935b9760cd04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 00:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 00:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 00:43:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:43:54 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 00:44:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 00:44:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 05:38:29 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 05:38:29 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 05:38:29 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 05:38:29 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 05:38:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 05:38:37 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 05:38:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 05:38:46 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 05:39:20 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 05:39:20 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 05:39:20 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 05:39:20 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 05:39:20 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 05:39:20 GMT
USER 8983
# Tue, 18 Apr 2023 05:39:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 05:39:21 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7affba4c9a33ed5dd050532c0d53e38b2c35c2fe490db721d943658feee4c914`  
		Last Modified: Tue, 18 Apr 2023 00:46:23 GMT  
		Size: 16.3 MB (16347011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fb5d08d03b0834295af88b5b911dca1240bcbdc3268dbc4c8ce24934ae017e`  
		Last Modified: Tue, 18 Apr 2023 00:47:26 GMT  
		Size: 46.6 MB (46632203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ef4a2443f5b89eae76a92c01bf3a006c986bb4fe658aa46a8dccc0bed2f523`  
		Last Modified: Tue, 18 Apr 2023 00:47:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e005372261eff41e611105a513fed9afaef08b30a879c639a8ac0efafd9300`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 4.9 MB (4901010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad0a251b15f3c813079323fdb45751b01c5753143b2c5dc1c6665bcc3e2680c`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 4.3 KB (4291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53da2eb3eae194651c65ebab849877740d6128968fd6e3f78f1a669b1ecb73d`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2462511e3bac8b859994f31534f2cfff6f8bfc787b5dc0909219b61ba839fdd1`  
		Last Modified: Tue, 18 Apr 2023 05:40:25 GMT  
		Size: 218.3 MB (218328276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7090d8a3f08936349556e936cfd4a9bfb2cd6661eeab03630417cee2cad95bfd`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 6.3 KB (6308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2` - linux; arm variant v7

```console
$ docker pull solr@sha256:b3c9697736d8208d626cff6651cc960c9311dd11f64a3eb1201af9d2d5b9ba63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307145944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1ab977a94d99fd58ad5909bb9e9369d6c96dbad9b2fce8b9a632c419774390`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:52:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:52:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:52:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:52:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:52:55 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:53:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:43:33 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 02:43:33 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:43:39 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 02:43:39 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 02:43:40 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:43:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 02:44:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 02:44:30 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 02:44:30 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:44:30 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:44:30 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:44:31 GMT
USER 8983
# Tue, 18 Apr 2023 02:44:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:44:31 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26020bb58aaff7bb6175448d285783e1d1698e726bcba90502c721abc88f2a2`  
		Last Modified: Tue, 18 Apr 2023 01:54:29 GMT  
		Size: 15.2 MB (15177669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07622852b9d8af8368242c298bb49668ea7975b2d9b6e4ac7c26bc7970508271`  
		Last Modified: Tue, 18 Apr 2023 01:55:29 GMT  
		Size: 44.8 MB (44843787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79339cee2747c7c082d0eaa5a711b4f5fd7a2875d6b6750d4bf589b282ae875`  
		Last Modified: Tue, 18 Apr 2023 01:55:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f70aeeae1860bbd48bdd953399d972be91807ea924ba06acdf3ba01345030`  
		Last Modified: Tue, 18 Apr 2023 02:45:34 GMT  
		Size: 4.2 MB (4195194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94952c7074a852730fda751b10e2166b7016df6315c67aedbdf50a8aab37d5ac`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 4.2 KB (4227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b56228b00077559f55a496496fc3498a3cd3387b66d45705967486a6283440`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a955106f4c93d7037f7715e10235bcccf43bdb83d6d00bd6e519230c2f0273c`  
		Last Modified: Tue, 18 Apr 2023 02:45:44 GMT  
		Size: 218.3 MB (218328154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0de5e28ecaf08af7bc911126dcbf7e95b93775829f90958146adab40f8b447`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:9c83437dd68f23bd3272fa16658b6bb0a96b4c47b0e19257d018071f1cbfe495
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311481859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0bcfc19e6f7e821e073ab8496a566a25ab40161cd530e90512c5f46ed1bf67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:40:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:40:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:41:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:41:31 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:41:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:41:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 03:21:22 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 03:21:23 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 03:21:28 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 03:21:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 03:21:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 03:21:43 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 03:22:14 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 03:22:16 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 03:22:16 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 03:22:16 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 03:22:16 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 03:22:16 GMT
USER 8983
# Tue, 18 Apr 2023 03:22:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 03:22:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269336393c4662b72ac4a2be29473801366e79f4db6c8b9944509f1903ee3fe6`  
		Last Modified: Tue, 18 Apr 2023 01:43:30 GMT  
		Size: 16.2 MB (16213349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775e69497bdf42d2ad7b39be6112c42f7fb711efa0036c55e9a5ddf8b30c244`  
		Last Modified: Tue, 18 Apr 2023 01:44:26 GMT  
		Size: 45.0 MB (44979459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff94c7a5594b10847f2895eb9f20938960ec3194f7398f5da8e801aff22ab00`  
		Last Modified: Tue, 18 Apr 2023 01:44:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3419bf7e5540a3bcd6132aa79f49429981574fb43627e2e617efd771123733e`  
		Last Modified: Tue, 18 Apr 2023 03:23:06 GMT  
		Size: 4.8 MB (4750130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f986cb8a544e5f5ed858bfd84e22a07cc5d8d5133bf126062e34097fb071cea9`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 4.3 KB (4335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46abce6c72ed3766b9f8dfbfadcecd21ca0597eef161bd3ef3b10408b72ae346`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbfb9f1a96f5d4bb8867ba070a31604ef992f2fe5672efd1775b3f3335be352`  
		Last Modified: Tue, 18 Apr 2023 03:23:15 GMT  
		Size: 218.3 MB (218328255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6099366efb07d013239cc98b209d1b555226441829877031336b84cc7f2f083`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 6.3 KB (6308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2` - linux; ppc64le

```console
$ docker pull solr@sha256:19c1b44a9bca9128a4069ed638cdcfc9c1798bba1421b33ab843e8f6e75096c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317067114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd4c81895762da00b4e9cd37462ffa750ebb80589f6511633158fd847760501`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:06:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:06:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:06:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:07:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:07:53 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:08:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:08:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:35:44 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 02:35:44 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 02:35:45 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 02:35:45 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 02:35:46 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 02:35:46 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:35:47 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:36:04 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 02:36:04 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 02:36:06 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:36:21 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 02:36:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 02:37:00 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 02:37:00 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:37:01 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:37:01 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:37:02 GMT
USER 8983
# Tue, 18 Apr 2023 02:37:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:37:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4018ee3c8b327c120bbf0427fb12e76c74cb054a92177aeeae16bcf0efa4e86`  
		Last Modified: Tue, 18 Apr 2023 01:11:24 GMT  
		Size: 17.6 MB (17582531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7790ee0621c15542c56b0e85f0263c81f9f6669f43fba1b253e99882262ffe6`  
		Last Modified: Tue, 18 Apr 2023 01:12:49 GMT  
		Size: 42.1 MB (42063861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41f4b7bd24a5b05c92949a1c05d6623acae52b5dfad264b0b2f5a039dd27309`  
		Last Modified: Tue, 18 Apr 2023 01:12:39 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15700e6ce1e1d806d636ec018e19719e2120a2c86c49fc3ea30b53bdd8cb4e53`  
		Last Modified: Tue, 18 Apr 2023 02:38:39 GMT  
		Size: 5.8 MB (5777224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1bdc6d63cfd771457f3b63241ca402866daafc083fa6a40856fa50462a5659`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86fa59a94ad403d12762e41a6b26d457d42e7e8b67d93566990919c5da301e`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecf09f805be54f9c957c79f858e1236520e512708a1e73ec27ab02efcb01494`  
		Last Modified: Tue, 18 Apr 2023 02:38:55 GMT  
		Size: 218.3 MB (218328288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7432224e033b9e67bcb4e97ac4c97c74022a8a9494d68f85c979018044e4a`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 6.3 KB (6306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2` - linux; s390x

```console
$ docker pull solr@sha256:389a866413fafae5f4a5524eadb24a3ffded326de4573a5a2ac7d590d86e76e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306661369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2623ddd1575fc5b45f9ddf500d45513829e78cd212412761a0a9945005a5b1ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:16:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:16:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:16:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:16:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:16:12 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:16:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:16:45 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 17:05:24 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 17:05:24 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 17:05:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 17:05:30 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 17:05:30 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 17:05:38 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 17:05:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 17:05:57 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 17:05:57 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 17:05:57 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 17:05:57 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 17:05:57 GMT
USER 8983
# Tue, 18 Apr 2023 17:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 17:05:57 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c307a57c5f07334cfab6db8f8324b0c9dff13121ec34d8db1d4a71e3529d4b5`  
		Last Modified: Tue, 18 Apr 2023 01:18:27 GMT  
		Size: 16.0 MB (16035272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edda216cc8ab33b8b4e53985609e8e8a98a3d295b6519ae9cb4f56fddbc35b6`  
		Last Modified: Tue, 18 Apr 2023 01:18:51 GMT  
		Size: 40.5 MB (40536784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bc476f2e4aba994464557beb4b38f1f1e73bf5cd02747e0f5c064af9c09bcc`  
		Last Modified: Tue, 18 Apr 2023 01:18:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7669fc3a7d75e3555f6ba98cd20d1ca196363ff6bad746e5027a023dc3dafe6f`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 4.7 MB (4730499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8708d9d2106caa9217180b74c334f5e6061dfa508e5f1612f4735fb8733b93f7`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a7defad728ae326c204388e49119c44a9cece1aad251d3224fed0f20fe9778`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 3.5 KB (3468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aebbf0c5137798a5b604fcd11bff32a718321a9ced08624b590f3b924ae29a0`  
		Last Modified: Tue, 18 Apr 2023 17:07:07 GMT  
		Size: 218.3 MB (218328179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bd21199ecdc92fc3907f7629a84a36f1a759a2855a8a4831c518182a02d91c`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 6.3 KB (6306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:8.11.2-slim`

```console
$ docker pull solr@sha256:213fd78add6f039335760ebdfaeb7843a01e7f3aa52a3350aff41e4a3e0521d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:8.11.2-slim` - linux; amd64

```console
$ docker pull solr@sha256:b210a1886da5e6bd04b978e092ad2282fefb2b2ab9e928465b5c6d4cad58497d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314801289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fee171281dcf64fb86a69dad1e9390dee50678fea5dc79f0259935b9760cd04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 00:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 00:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 00:43:22 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:43:54 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 00:44:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 00:44:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 05:38:29 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 05:38:29 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 05:38:29 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 05:38:29 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 05:38:30 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 05:38:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 05:38:37 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 05:38:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 05:38:46 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 05:39:20 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 05:39:20 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 05:39:20 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 05:39:20 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 05:39:20 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 05:39:20 GMT
USER 8983
# Tue, 18 Apr 2023 05:39:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 05:39:21 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7affba4c9a33ed5dd050532c0d53e38b2c35c2fe490db721d943658feee4c914`  
		Last Modified: Tue, 18 Apr 2023 00:46:23 GMT  
		Size: 16.3 MB (16347011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fb5d08d03b0834295af88b5b911dca1240bcbdc3268dbc4c8ce24934ae017e`  
		Last Modified: Tue, 18 Apr 2023 00:47:26 GMT  
		Size: 46.6 MB (46632203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ef4a2443f5b89eae76a92c01bf3a006c986bb4fe658aa46a8dccc0bed2f523`  
		Last Modified: Tue, 18 Apr 2023 00:47:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e005372261eff41e611105a513fed9afaef08b30a879c639a8ac0efafd9300`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 4.9 MB (4901010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad0a251b15f3c813079323fdb45751b01c5753143b2c5dc1c6665bcc3e2680c`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 4.3 KB (4291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53da2eb3eae194651c65ebab849877740d6128968fd6e3f78f1a669b1ecb73d`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2462511e3bac8b859994f31534f2cfff6f8bfc787b5dc0909219b61ba839fdd1`  
		Last Modified: Tue, 18 Apr 2023 05:40:25 GMT  
		Size: 218.3 MB (218328276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7090d8a3f08936349556e936cfd4a9bfb2cd6661eeab03630417cee2cad95bfd`  
		Last Modified: Tue, 18 Apr 2023 05:40:16 GMT  
		Size: 6.3 KB (6308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2-slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:b3c9697736d8208d626cff6651cc960c9311dd11f64a3eb1201af9d2d5b9ba63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307145944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1ab977a94d99fd58ad5909bb9e9369d6c96dbad9b2fce8b9a632c419774390`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:52:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:52:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:52:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:52:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:52:55 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:53:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:53:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:43:33 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 02:43:33 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:43:33 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:43:39 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 02:43:39 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 02:43:40 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:43:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 02:44:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 02:44:30 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 02:44:30 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:44:30 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:44:30 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:44:31 GMT
USER 8983
# Tue, 18 Apr 2023 02:44:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:44:31 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26020bb58aaff7bb6175448d285783e1d1698e726bcba90502c721abc88f2a2`  
		Last Modified: Tue, 18 Apr 2023 01:54:29 GMT  
		Size: 15.2 MB (15177669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07622852b9d8af8368242c298bb49668ea7975b2d9b6e4ac7c26bc7970508271`  
		Last Modified: Tue, 18 Apr 2023 01:55:29 GMT  
		Size: 44.8 MB (44843787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79339cee2747c7c082d0eaa5a711b4f5fd7a2875d6b6750d4bf589b282ae875`  
		Last Modified: Tue, 18 Apr 2023 01:55:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254f70aeeae1860bbd48bdd953399d972be91807ea924ba06acdf3ba01345030`  
		Last Modified: Tue, 18 Apr 2023 02:45:34 GMT  
		Size: 4.2 MB (4195194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94952c7074a852730fda751b10e2166b7016df6315c67aedbdf50a8aab37d5ac`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 4.2 KB (4227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b56228b00077559f55a496496fc3498a3cd3387b66d45705967486a6283440`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a955106f4c93d7037f7715e10235bcccf43bdb83d6d00bd6e519230c2f0273c`  
		Last Modified: Tue, 18 Apr 2023 02:45:44 GMT  
		Size: 218.3 MB (218328154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0de5e28ecaf08af7bc911126dcbf7e95b93775829f90958146adab40f8b447`  
		Last Modified: Tue, 18 Apr 2023 02:45:33 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:9c83437dd68f23bd3272fa16658b6bb0a96b4c47b0e19257d018071f1cbfe495
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311481859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0bcfc19e6f7e821e073ab8496a566a25ab40161cd530e90512c5f46ed1bf67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:40:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:40:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:41:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:41:31 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:41:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:41:55 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 03:21:22 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 03:21:23 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 03:21:23 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 03:21:28 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 03:21:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 03:21:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 03:21:43 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 03:22:14 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 03:22:16 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 03:22:16 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 03:22:16 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 03:22:16 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 03:22:16 GMT
USER 8983
# Tue, 18 Apr 2023 03:22:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 03:22:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269336393c4662b72ac4a2be29473801366e79f4db6c8b9944509f1903ee3fe6`  
		Last Modified: Tue, 18 Apr 2023 01:43:30 GMT  
		Size: 16.2 MB (16213349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5775e69497bdf42d2ad7b39be6112c42f7fb711efa0036c55e9a5ddf8b30c244`  
		Last Modified: Tue, 18 Apr 2023 01:44:26 GMT  
		Size: 45.0 MB (44979459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff94c7a5594b10847f2895eb9f20938960ec3194f7398f5da8e801aff22ab00`  
		Last Modified: Tue, 18 Apr 2023 01:44:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3419bf7e5540a3bcd6132aa79f49429981574fb43627e2e617efd771123733e`  
		Last Modified: Tue, 18 Apr 2023 03:23:06 GMT  
		Size: 4.8 MB (4750130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f986cb8a544e5f5ed858bfd84e22a07cc5d8d5133bf126062e34097fb071cea9`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 4.3 KB (4335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46abce6c72ed3766b9f8dfbfadcecd21ca0597eef161bd3ef3b10408b72ae346`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbfb9f1a96f5d4bb8867ba070a31604ef992f2fe5672efd1775b3f3335be352`  
		Last Modified: Tue, 18 Apr 2023 03:23:15 GMT  
		Size: 218.3 MB (218328255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6099366efb07d013239cc98b209d1b555226441829877031336b84cc7f2f083`  
		Last Modified: Tue, 18 Apr 2023 03:23:05 GMT  
		Size: 6.3 KB (6308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:19c1b44a9bca9128a4069ed638cdcfc9c1798bba1421b33ab843e8f6e75096c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317067114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd4c81895762da00b4e9cd37462ffa750ebb80589f6511633158fd847760501`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:06:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:06:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:06:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:07:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:07:53 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:08:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:08:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:35:44 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 02:35:44 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 02:35:45 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 02:35:45 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 02:35:46 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 02:35:46 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:35:47 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:36:04 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 02:36:04 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 02:36:06 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:36:21 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 02:36:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 02:37:00 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 02:37:00 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:37:01 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:37:01 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:37:02 GMT
USER 8983
# Tue, 18 Apr 2023 02:37:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:37:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4018ee3c8b327c120bbf0427fb12e76c74cb054a92177aeeae16bcf0efa4e86`  
		Last Modified: Tue, 18 Apr 2023 01:11:24 GMT  
		Size: 17.6 MB (17582531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7790ee0621c15542c56b0e85f0263c81f9f6669f43fba1b253e99882262ffe6`  
		Last Modified: Tue, 18 Apr 2023 01:12:49 GMT  
		Size: 42.1 MB (42063861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41f4b7bd24a5b05c92949a1c05d6623acae52b5dfad264b0b2f5a039dd27309`  
		Last Modified: Tue, 18 Apr 2023 01:12:39 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15700e6ce1e1d806d636ec018e19719e2120a2c86c49fc3ea30b53bdd8cb4e53`  
		Last Modified: Tue, 18 Apr 2023 02:38:39 GMT  
		Size: 5.8 MB (5777224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1bdc6d63cfd771457f3b63241ca402866daafc083fa6a40856fa50462a5659`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c86fa59a94ad403d12762e41a6b26d457d42e7e8b67d93566990919c5da301e`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecf09f805be54f9c957c79f858e1236520e512708a1e73ec27ab02efcb01494`  
		Last Modified: Tue, 18 Apr 2023 02:38:55 GMT  
		Size: 218.3 MB (218328288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7432224e033b9e67bcb4e97ac4c97c74022a8a9494d68f85c979018044e4a`  
		Last Modified: Tue, 18 Apr 2023 02:38:37 GMT  
		Size: 6.3 KB (6306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2-slim` - linux; s390x

```console
$ docker pull solr@sha256:389a866413fafae5f4a5524eadb24a3ffded326de4573a5a2ac7d590d86e76e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306661369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2623ddd1575fc5b45f9ddf500d45513829e78cd212412761a0a9945005a5b1ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:16:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:16:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:16:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:16:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:16:12 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 18 Apr 2023 01:16:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:16:45 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 17:05:24 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 18 Apr 2023 17:05:24 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 17:05:25 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 17:05:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 18 Apr 2023 17:05:30 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 18 Apr 2023 17:05:30 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 17:05:38 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 18 Apr 2023 17:05:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 18 Apr 2023 17:05:57 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 18 Apr 2023 17:05:57 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 17:05:57 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 17:05:57 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 17:05:57 GMT
USER 8983
# Tue, 18 Apr 2023 17:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 17:05:57 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c307a57c5f07334cfab6db8f8324b0c9dff13121ec34d8db1d4a71e3529d4b5`  
		Last Modified: Tue, 18 Apr 2023 01:18:27 GMT  
		Size: 16.0 MB (16035272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edda216cc8ab33b8b4e53985609e8e8a98a3d295b6519ae9cb4f56fddbc35b6`  
		Last Modified: Tue, 18 Apr 2023 01:18:51 GMT  
		Size: 40.5 MB (40536784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bc476f2e4aba994464557beb4b38f1f1e73bf5cd02747e0f5c064af9c09bcc`  
		Last Modified: Tue, 18 Apr 2023 01:18:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7669fc3a7d75e3555f6ba98cd20d1ca196363ff6bad746e5027a023dc3dafe6f`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 4.7 MB (4730499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8708d9d2106caa9217180b74c334f5e6061dfa508e5f1612f4735fb8733b93f7`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a7defad728ae326c204388e49119c44a9cece1aad251d3224fed0f20fe9778`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 3.5 KB (3468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aebbf0c5137798a5b604fcd11bff32a718321a9ced08624b590f3b924ae29a0`  
		Last Modified: Tue, 18 Apr 2023 17:07:07 GMT  
		Size: 218.3 MB (218328179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bd21199ecdc92fc3907f7629a84a36f1a759a2855a8a4831c518182a02d91c`  
		Last Modified: Tue, 18 Apr 2023 17:06:59 GMT  
		Size: 6.3 KB (6306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:9`

```console
$ docker pull solr@sha256:6a63019e5694591e2d1c53d56cdcba819235adbd1e85d91f0f82cc7562ea1ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:9` - linux; amd64

```console
$ docker pull solr@sha256:cbee52e4b6a1e30d450e8ca19402c3bc15d4d8e8a75ca8501cb0f7f642cc76ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.9 MB (374859971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d43c32e8ee6e715af99f55ba48e134125af6eadbc175932523f25a1070ce4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:44:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:46:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:46:48 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:47:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:47:22 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:07 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:52 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:20:53 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:20:54 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:20:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:20:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:21:03 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:21:03 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:21:03 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:21:03 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:21:04 GMT
USER 8983
# Fri, 24 Mar 2023 20:21:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:21:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182a611d05b01879f065473c49fb968b8d30312f931350ea07af1c46aa8b4f9`  
		Last Modified: Thu, 16 Mar 2023 02:53:08 GMT  
		Size: 17.0 MB (16975402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb51f9f63778bb9fb97f2cb054b54dfc5098aba2931664a12930c35cf464ca6`  
		Last Modified: Thu, 16 Mar 2023 02:54:00 GMT  
		Size: 46.9 MB (46935467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1365afd8cae0153f1c2bfcf8a4c9b78f2e6e0f18431b0460c63c1fede7507fee`  
		Last Modified: Thu, 16 Mar 2023 02:53:53 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b70190cd6e82c4ac613c9f0f9bf4e42155528b445617672bcd7a211b2a2104`  
		Last Modified: Fri, 24 Mar 2023 20:21:43 GMT  
		Size: 278.7 MB (278678830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c984f04f09ad32d618a63f426eb4127534ca414910aa8b56da2355a3bcf17c17`  
		Last Modified: Fri, 24 Mar 2023 20:21:31 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888b9068f218433d417da0cd83cca3863ad2cbea9bab37c09fc52a63fab6206e`  
		Last Modified: Fri, 24 Mar 2023 20:21:31 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1599d0444630b3ac11f8d61742ff79acaaec1b9cfcca5e176b131ef54c22bd`  
		Last Modified: Fri, 24 Mar 2023 20:21:32 GMT  
		Size: 8.3 KB (8264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbc52fa8b34cbd17b27c7c562e83344a928724a395e74a740d6bcfbd0aca1e8`  
		Last Modified: Fri, 24 Mar 2023 20:21:32 GMT  
		Size: 1.8 MB (1827370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9` - linux; arm variant v7

```console
$ docker pull solr@sha256:7ce35f5dfe8a54b79e4886b38ee7bbae1768c5080b38dd88007711f1a730ca97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.0 MB (368994236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0c33c02e827728f7408559ce07896fbcd7ef42a58bd47bd0c340d122ef7c70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:46:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:46:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:46:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:49:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:49:36 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:50:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:50:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 21:14:57 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 21:14:57 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:15:46 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 21:15:48 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 21:15:49 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 21:15:49 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 21:15:50 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 21:15:59 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 21:16:00 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 21:16:00 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 21:16:00 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 21:16:00 GMT
USER 8983
# Fri, 24 Mar 2023 21:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 21:16:00 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:cba1fa3bcdf4f746dcf5b8f86874cee4a6eff75dd5c5cd29e4c912574b12a1c6`  
		Last Modified: Thu, 09 Mar 2023 04:41:14 GMT  
		Size: 27.0 MB (27025397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85169cff2ee4bc04fcfaf94a937435e69eb27ca38bf1dcbd04593cccacf0d702`  
		Last Modified: Thu, 16 Mar 2023 02:56:32 GMT  
		Size: 17.1 MB (17093778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be72bd479c96978965e7a3ad3512673e6ca3b26714713ca967a807e2c0bcdb7e`  
		Last Modified: Thu, 16 Mar 2023 02:57:28 GMT  
		Size: 44.5 MB (44528811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5725cdfe807b737e733d3d3a443ffd37aef0141ba7a33fb98b334c479486085`  
		Last Modified: Thu, 16 Mar 2023 02:57:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f40c0125b4d5835619a97a6e8aa526c71d7c68b45f248b530ebb09d2d1570c6`  
		Last Modified: Fri, 24 Mar 2023 21:16:36 GMT  
		Size: 278.7 MB (278680032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c884c5595959c80781c31e89baa334da69c61145587cecf73ae8777f044fbb01`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 4.2 KB (4224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387e1ea0fbb6ae2834c227fdf0661b61a1dbe74918fddc3fb294bb4dbbbce8b9`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4b5c915fbddf45760ab4310f38f8bce027f6be8d21539defc6c49238e0d1d9`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 8.3 KB (8259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c5e2d209b82002244ea91d52f9d395d4e38adde0830ca8a1a014fd6a0fb50b`  
		Last Modified: Fri, 24 Mar 2023 21:16:21 GMT  
		Size: 1.7 MB (1653357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:58619b9500a6637702a27985f2cf8b17cb13dae6c2673f3abaa9a1bd824277ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.6 MB (373587696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f72e1df4e02c02f553d7d54dd64951829dbdd59095775a6634ddce70eadc8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:52:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:52:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:52:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:55:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:55:04 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:55:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:55:30 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:47:31 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:47:31 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:48:14 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:48:17 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:48:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:48:17 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:48:17 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:48:18 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:48:18 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:48:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:48:27 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:48:27 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:48:27 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:48:28 GMT
USER 8983
# Fri, 24 Mar 2023 20:48:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:48:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40b70fd7935308ad0e072e7e06ec8c3abdc59beae70ca716dcd04e971680865`  
		Last Modified: Thu, 16 Mar 2023 02:00:42 GMT  
		Size: 18.4 MB (18400790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33dd5efa5ce73b25dc0236fcd408527b63e42c87e6da9672a356731004b8949`  
		Last Modified: Thu, 16 Mar 2023 02:01:25 GMT  
		Size: 46.4 MB (46421360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ce9280353ea6c4511dc5378e2f0f4742d499bf6df15c8d10804513c8c5115a`  
		Last Modified: Thu, 16 Mar 2023 02:01:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab85ed965ce21582560c60a815ae59ae9cf0fcb5c9270ba02dfc5ca1c135b44f`  
		Last Modified: Fri, 24 Mar 2023 20:49:04 GMT  
		Size: 278.7 MB (278678702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47faea25001b6a9178cab60304409e81d636878232dda7e76d519e7490bbc9`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7792e9b554723df7cdd9593ee715d8fe16cfec71a28c58e0b01e2534e7f2c8`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9435de9f76e1e09e2078c456e20cd6a83a757671ecc43398fed205b323cb3c6b`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 8.3 KB (8261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fc7a7f4116bfd1b88180e25c33fa7c4d571df7caad6ffebbec7786b32b2738`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 1.7 MB (1686320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9` - linux; ppc64le

```console
$ docker pull solr@sha256:f10e0c22e5adec6e85249f7eac5f7a5f930872dbd32a9cd7c770ec7ab6077b61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.3 MB (381276492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08713b2a6558c371eb5008de184f2ae763ef7c3a322e2d740c9665f599eb2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:57:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 03:57:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 03:57:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 04:03:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:03:28 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 04:04:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 04:04:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:16:55 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:18:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:18:18 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:18:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:18:21 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:18:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:18:24 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:18:25 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:18:40 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:18:41 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:18:41 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:18:41 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:18:41 GMT
USER 8983
# Fri, 24 Mar 2023 20:18:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:18:42 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c06c33e4689e5957d961321ac18da32bea369d2eccc9173c9ad8b517f802ea`  
		Last Modified: Thu, 16 Mar 2023 04:14:09 GMT  
		Size: 18.3 MB (18257665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75be9792a67101a27b125eb6a0e465b760b4302cd2fbf3cf19338303bcfe803`  
		Last Modified: Thu, 16 Mar 2023 04:15:24 GMT  
		Size: 46.8 MB (46780948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba3f99059088b7aca45113a2e84d92786ffffd7b3920e17bc78082f1ca41023`  
		Last Modified: Thu, 16 Mar 2023 04:15:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a80e5b79ed57a03fbca62529db243f85c92ae5df2321c4e9f1224711e54a0d8`  
		Last Modified: Fri, 24 Mar 2023 20:19:29 GMT  
		Size: 278.7 MB (278679501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a83b0eea3048a8cc5ee14c0ed706cd75212e6513827c6e50ee8514b3a37ffa`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfda90d0edd877ecc2717bf59c6b25f8810ed05202ab28ba588f60de2cc3332e`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffae90319602b89f29babd93a389ad3dcb0acd2637266cdb4f1e0e4b02309a2`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 8.3 KB (8264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7a5d7ac7a4e26a6795ad596e099b124de0249d7a8cd31eff56a0786195d720`  
		Last Modified: Fri, 24 Mar 2023 20:19:07 GMT  
		Size: 1.8 MB (1833711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9` - linux; s390x

```console
$ docker pull solr@sha256:55d3908647c17e61e6cc73ac71deba6d9ab2a161bd4aa7b6ea15c7a7a75fab5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369606057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1685dca8b24c2c5e320e5a7ef4c2bb2431ea293974475f5458fee07495a73e61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:06:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:06:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:06:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:07:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:07:59 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:08:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:08:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:42:43 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:43:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:43:20 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:43:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:43:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:43:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:43:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:43:27 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:43:27 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:43:27 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:43:28 GMT
USER 8983
# Fri, 24 Mar 2023 20:43:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:43:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2c7366af510b72cc0b3456fb93cfa0bfc76f7d383db5cb315967e7b1ce2e0c42`  
		Last Modified: Thu, 16 Mar 2023 02:02:40 GMT  
		Size: 28.6 MB (28647599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d28ae42a862e9773a02317b5a0eeb71ddfe3a887bb001c8f23a2786c926287`  
		Last Modified: Thu, 16 Mar 2023 02:13:35 GMT  
		Size: 16.8 MB (16753284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6bfb39a3fef3f50b4d32c5f857a5b18f142a97de79cf264830c8ca2b9864f7`  
		Last Modified: Thu, 16 Mar 2023 02:14:17 GMT  
		Size: 43.7 MB (43738850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d39319012144c92bc4367a44b2f3e4e953b589c17b4ca366d17c8743bff813f`  
		Last Modified: Thu, 16 Mar 2023 02:14:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f074327dc8f7e760db6a5b895eb86f852bfc333785586ee10413da37f3f222`  
		Last Modified: Fri, 24 Mar 2023 20:44:10 GMT  
		Size: 278.7 MB (278679125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b051ae3be65d0725f3676e0baa40a2410ad18f0aff69131fa9715c782378cb77`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0557baee179cb29c3fd717a2a7bb1914e6f0113559f232f327cda5d986fd9a91`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd59caab82c0a6e67e3eeed26458e15e132ad27eb419aa32240ac3ac08575f5e`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 8.3 KB (8259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89595dcc22b7df58249dbec6b0679a7aa1651e536af2a463aa9d3226f9acf21d`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 1.8 MB (1774235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:9.0`

```console
$ docker pull solr@sha256:37cacec66c3267249175c0e6306b490dba2615aa106da45a78651ee0adab8984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:9.0` - linux; amd64

```console
$ docker pull solr@sha256:f18526a050126b6147881c8dd4d460a4bbdfee8961af0ff48e4191f37ba9c6b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324868649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ed6d388f891f47949ba624eca0e87d9d960ff664167f65447e228a008442f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 00:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 00:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 00:44:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:44:48 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 00:45:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 00:45:16 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 05:36:36 GMT
ARG SOLR_VERSION=9.0.0
# Tue, 18 Apr 2023 05:36:36 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Tue, 18 Apr 2023 05:36:36 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Tue, 18 Apr 2023 05:36:37 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 05:36:37 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 05:36:37 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 05:36:37 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 05:36:37 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 05:38:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 05:38:15 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 05:38:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 05:38:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 05:38:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 05:38:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 05:38:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 05:38:16 GMT
LABEL org.opencontainers.image.version=9.0.0
# Tue, 18 Apr 2023 05:38:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 05:38:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 05:38:17 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 05:38:17 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 05:38:18 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 05:38:23 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 05:38:23 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 05:38:23 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 05:38:23 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 05:38:23 GMT
USER solr
# Tue, 18 Apr 2023 05:38:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 05:38:23 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b493027a1bf3e6a19b932ebe3c6dbfe19dc6a4583dfe39282977a57c89b31e87`  
		Last Modified: Tue, 18 Apr 2023 00:47:39 GMT  
		Size: 20.1 MB (20096839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02938177297ab7e29f7435f1f8092e05942dc412fbdfa6c1421589d8ef0adb57`  
		Last Modified: Tue, 18 Apr 2023 00:48:08 GMT  
		Size: 46.9 MB (46937043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e9595e3a57ad3c2eaf905104408a625b61809733c58a795c86405e275aea0b`  
		Last Modified: Tue, 18 Apr 2023 00:48:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98193c6fa8ee72e820dc54e8630cbd02c47cc281df0d68e994ca080d99640121`  
		Last Modified: Tue, 18 Apr 2023 05:40:08 GMT  
		Size: 227.7 MB (227662006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e117f25a692ce00f5f650f780a4628128f67b5147b2d108763cd51a15fece7`  
		Last Modified: Tue, 18 Apr 2023 05:39:57 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c44df4002d9a5cc50c30572f7ce52330b70e5bd0dabb2e428900a6668689ede`  
		Last Modified: Tue, 18 Apr 2023 05:39:57 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f2037c2a933d185399697810bbaa8a464d0ff063b932b21edfcaf641068d6b`  
		Last Modified: Tue, 18 Apr 2023 05:39:57 GMT  
		Size: 7.9 KB (7908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb7c6696693b299c6ca775396a3f776e19489087ceb99fbb661b46714595d73`  
		Last Modified: Tue, 18 Apr 2023 05:39:58 GMT  
		Size: 1.6 MB (1581615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0` - linux; arm variant v7

```console
$ docker pull solr@sha256:d87f0589f7c2845e924c43207a651338c16c97d7d6dc4bcec48e5b81333fa40b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317130504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7885b034631769de505cfa7a2c137ed4ca3a1bc14500408f4f79a0b4043f906`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:52:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:52:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:52:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:53:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:53:36 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:54:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:54:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:42:24 GMT
ARG SOLR_VERSION=9.0.0
# Tue, 18 Apr 2023 02:42:24 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Tue, 18 Apr 2023 02:42:24 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Tue, 18 Apr 2023 02:42:24 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:42:24 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:42:24 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 02:42:24 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 02:42:25 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 02:43:12 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 02:43:13 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 02:43:13 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 02:43:14 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 02:43:14 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 02:43:14 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 02:43:14 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 02:43:14 GMT
LABEL org.opencontainers.image.version=9.0.0
# Tue, 18 Apr 2023 02:43:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 02:43:14 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 02:43:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:43:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 02:43:16 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 02:43:20 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 02:43:20 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:43:20 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:43:20 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:43:20 GMT
USER solr
# Tue, 18 Apr 2023 02:43:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:43:20 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85796ae94aa6103041abcc6b06ff12a50d94cadaf6e06eb70a7394c3872a6748`  
		Last Modified: Tue, 18 Apr 2023 01:55:40 GMT  
		Size: 19.5 MB (19465888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cce25c2e3b898f27ed23666a27be2cf47a2d62ace6c9630292dd9db7e2c67a`  
		Last Modified: Tue, 18 Apr 2023 01:56:11 GMT  
		Size: 44.5 MB (44529877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc071ae82a251704f7fd76936abcd7ba3254e014f37f54c2a0e3382398a9027`  
		Last Modified: Tue, 18 Apr 2023 01:56:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729935b9475e1a5c9d749c462c66dc4feeef3ac2ab6eb0b5210a8da556334f9f`  
		Last Modified: Tue, 18 Apr 2023 02:45:25 GMT  
		Size: 227.1 MB (227140646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0d9bcf8720cc8ac9d25548c42d3e312e7bf657a9ae9bb39e70b8b28580cc09`  
		Last Modified: Tue, 18 Apr 2023 02:45:13 GMT  
		Size: 4.2 KB (4225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edb4a37ae5a67ae98b159249438983fda2f9f94121d0f382fe6f8f656554afd`  
		Last Modified: Tue, 18 Apr 2023 02:45:12 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfdabd208deb1701eae64a822800fc6606c1cf3eabe04c7b1fafba629896b05`  
		Last Modified: Tue, 18 Apr 2023 02:45:12 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fbb7c77a9b97e47e625e18d1437411da4080b4ea574e19c01f10dde13d5f1a`  
		Last Modified: Tue, 18 Apr 2023 02:45:13 GMT  
		Size: 1.4 MB (1394613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:04b463901ac8bde6a6272968ee59681b13ac42b5fc6f51354aa63e950303c655
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 MB (323539610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7d64830b601b2d2e151a405e707709593e852282532226766335d39e6f8d9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:40:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:40:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:42:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:42:18 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:42:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:42:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 03:20:25 GMT
ARG SOLR_VERSION=9.0.0
# Tue, 18 Apr 2023 03:20:25 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Tue, 18 Apr 2023 03:20:25 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Tue, 18 Apr 2023 03:20:26 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 03:20:26 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 03:20:26 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 03:20:26 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 03:20:26 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 03:21:07 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 03:21:08 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 03:21:08 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 03:21:09 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 03:21:09 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 03:21:09 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 03:21:09 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 03:21:09 GMT
LABEL org.opencontainers.image.version=9.0.0
# Tue, 18 Apr 2023 03:21:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 03:21:09 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 03:21:10 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 03:21:10 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 03:21:11 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 03:21:14 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 03:21:14 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 03:21:14 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 03:21:14 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 03:21:14 GMT
USER solr
# Tue, 18 Apr 2023 03:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 03:21:15 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f855dc454f40dbe47d375c509772787d9d27ff505e14349af4f2e3944f28f75`  
		Last Modified: Tue, 18 Apr 2023 01:44:38 GMT  
		Size: 20.8 MB (20815202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c91968e85b36d056d961163f2b9155edf8119f19516132648c5ecae886bcb3`  
		Last Modified: Tue, 18 Apr 2023 01:45:04 GMT  
		Size: 46.4 MB (46422365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6e32ee26ed47aaac9a5a70c0af73a59858c966aa6646cc3b0151c938bf39b1`  
		Last Modified: Tue, 18 Apr 2023 01:44:58 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0524d79428e8b6d258e182e12c143bc4636644497eb2f713d60bdfc592edcd6`  
		Last Modified: Tue, 18 Apr 2023 03:22:57 GMT  
		Size: 227.6 MB (227649927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02d66c108983824382ae01d655355e198973423b56fe3eac73aee5179245f16`  
		Last Modified: Tue, 18 Apr 2023 03:22:48 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2681b3124697ad3547533a9029d2e44719236d1c5eae31b97c12ac3d5ea9b6`  
		Last Modified: Tue, 18 Apr 2023 03:22:48 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b070826d2cc919b0a9d715e8dc23ac37c6b5068504db8966f7a4ea17da59adf`  
		Last Modified: Tue, 18 Apr 2023 03:22:48 GMT  
		Size: 7.9 KB (7899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c094f24ea3e7d5f503111a9b1379c03432bce9153ceba74dd261b293c853d1f`  
		Last Modified: Tue, 18 Apr 2023 03:22:48 GMT  
		Size: 1.4 MB (1443110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0` - linux; ppc64le

```console
$ docker pull solr@sha256:a9475313e73f548e27cdf2bc5e191e9396e588873e85d262d8afcb1355eb5ff2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332285619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f67f099c986d27845fa804471808cfa221c43cd40b3a871d7d61266dc897671`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:06:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:06:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:06:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:09:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:09:19 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:10:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:10:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:34:21 GMT
ARG SOLR_VERSION=9.0.0
# Tue, 18 Apr 2023 02:34:22 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Tue, 18 Apr 2023 02:34:23 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Tue, 18 Apr 2023 02:34:24 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:34:24 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:34:24 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 02:34:25 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 02:34:25 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 02:35:12 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 02:35:15 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 02:35:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 02:35:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 02:35:17 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 02:35:17 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 02:35:17 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 02:35:17 GMT
LABEL org.opencontainers.image.version=9.0.0
# Tue, 18 Apr 2023 02:35:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 02:35:18 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 02:35:19 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:35:20 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 02:35:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 02:35:31 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 02:35:31 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:35:31 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:35:32 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:35:32 GMT
USER solr
# Tue, 18 Apr 2023 02:35:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:35:33 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d16c8f7fe3c69e12b82f6ead20825685acccc07c7db20352690c45095874956`  
		Last Modified: Tue, 18 Apr 2023 01:13:05 GMT  
		Size: 22.1 MB (22066207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2766b2ad3fad77d8cd1101de070f2cbc3f36ed8fdef8d95dce041bca895bd1f`  
		Last Modified: Tue, 18 Apr 2023 01:13:48 GMT  
		Size: 46.8 MB (46780913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ba72e32ba8796d6aa8e1b06921ca5c30137cd512ca4f20ca3a6525e2385cd2`  
		Last Modified: Tue, 18 Apr 2023 01:13:36 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4a7787e814f2522f6da4ac6a7d7d6f8d7044671f7a21a0d9367db996a2091e`  
		Last Modified: Tue, 18 Apr 2023 02:38:28 GMT  
		Size: 228.5 MB (228520977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e9f7f73cc13eaa6b8dcc824380daa8713edf23035070230bf611c9852556f`  
		Last Modified: Tue, 18 Apr 2023 02:38:09 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7351a9bd649a1fca781ccf335ec1846158f67665b5c6bea8f4df0981daf1ee`  
		Last Modified: Tue, 18 Apr 2023 02:38:09 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001b4d4b51c19699698e864b870de173145ae13112455690b827d435e3e14707`  
		Last Modified: Tue, 18 Apr 2023 02:38:09 GMT  
		Size: 7.9 KB (7901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2420793c8e6a25c0ea6bf5ae7f54b01e975bcea880317865fecfb8a53a586b`  
		Last Modified: Tue, 18 Apr 2023 02:38:10 GMT  
		Size: 1.6 MB (1603967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0` - linux; s390x

```console
$ docker pull solr@sha256:b0b10f10c4b3f0a46e01b9cdd9bbda792ddf06647479c6c57aecc0989f1bd0b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.4 MB (319373122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92814c5d4520c50905c171e10736316604fa13798095d7fa3c5209841b80063`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:16:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:16:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:16:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:17:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:17:10 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:17:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:17:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_VERSION=9.0.0
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 17:05:09 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.version=9.0.0
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 17:05:13 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 17:05:14 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 17:05:14 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 17:05:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 17:05:18 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 17:05:18 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 17:05:18 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 17:05:18 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 17:05:18 GMT
USER solr
# Tue, 18 Apr 2023 17:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 17:05:19 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf6c28f706c8f54c079ff27fe5409527f68c7463df6adf843d835f265547cf5`  
		Last Modified: Tue, 18 Apr 2023 01:19:02 GMT  
		Size: 19.5 MB (19532693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef55f447b7c061c28ebda47f938df25295b85f1e950785fbf350c166ce482a24`  
		Last Modified: Tue, 18 Apr 2023 01:19:26 GMT  
		Size: 43.7 MB (43739777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6627870afe22e0029eee4a5cb3c10c040a070bcd6c443b86248fb66151725bb6`  
		Last Modified: Tue, 18 Apr 2023 01:19:20 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cc4d3f8fcdf8e2799184cf4370edd3318456a1ff69eb195086ae7993030bb6`  
		Last Modified: Tue, 18 Apr 2023 17:06:52 GMT  
		Size: 227.6 MB (227575740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27aea3cbfd9d56f917e11ceff90c24df7e00c872834596a1f8f971385880ef6`  
		Last Modified: Tue, 18 Apr 2023 17:06:41 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e345e4d33bc7de7e08d81012d30f0956b9b1d20037ba6dfe29242ef94ee20`  
		Last Modified: Tue, 18 Apr 2023 17:06:41 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ee5fd9a7f4e529237b057d12170b75ce61ae19bc7f4c60834800e5a7b04202`  
		Last Modified: Tue, 18 Apr 2023 17:06:41 GMT  
		Size: 7.9 KB (7899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb32a39cbc8de15dfbda608e5bd78b87c49719651e5556c9c472b328c9fe535`  
		Last Modified: Tue, 18 Apr 2023 17:06:41 GMT  
		Size: 1.5 MB (1495929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:9.0.0`

```console
$ docker pull solr@sha256:37cacec66c3267249175c0e6306b490dba2615aa106da45a78651ee0adab8984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:9.0.0` - linux; amd64

```console
$ docker pull solr@sha256:f18526a050126b6147881c8dd4d460a4bbdfee8961af0ff48e4191f37ba9c6b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324868649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ed6d388f891f47949ba624eca0e87d9d960ff664167f65447e228a008442f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 00:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 00:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 00:44:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:44:48 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 00:45:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 00:45:16 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 05:36:36 GMT
ARG SOLR_VERSION=9.0.0
# Tue, 18 Apr 2023 05:36:36 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Tue, 18 Apr 2023 05:36:36 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Tue, 18 Apr 2023 05:36:37 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 05:36:37 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 05:36:37 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 05:36:37 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 05:36:37 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 05:38:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 05:38:15 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 05:38:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 05:38:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 05:38:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 05:38:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 05:38:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 05:38:16 GMT
LABEL org.opencontainers.image.version=9.0.0
# Tue, 18 Apr 2023 05:38:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 05:38:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 05:38:17 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 05:38:17 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 05:38:18 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 05:38:23 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 05:38:23 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 05:38:23 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 05:38:23 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 05:38:23 GMT
USER solr
# Tue, 18 Apr 2023 05:38:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 05:38:23 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b493027a1bf3e6a19b932ebe3c6dbfe19dc6a4583dfe39282977a57c89b31e87`  
		Last Modified: Tue, 18 Apr 2023 00:47:39 GMT  
		Size: 20.1 MB (20096839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02938177297ab7e29f7435f1f8092e05942dc412fbdfa6c1421589d8ef0adb57`  
		Last Modified: Tue, 18 Apr 2023 00:48:08 GMT  
		Size: 46.9 MB (46937043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e9595e3a57ad3c2eaf905104408a625b61809733c58a795c86405e275aea0b`  
		Last Modified: Tue, 18 Apr 2023 00:48:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98193c6fa8ee72e820dc54e8630cbd02c47cc281df0d68e994ca080d99640121`  
		Last Modified: Tue, 18 Apr 2023 05:40:08 GMT  
		Size: 227.7 MB (227662006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e117f25a692ce00f5f650f780a4628128f67b5147b2d108763cd51a15fece7`  
		Last Modified: Tue, 18 Apr 2023 05:39:57 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c44df4002d9a5cc50c30572f7ce52330b70e5bd0dabb2e428900a6668689ede`  
		Last Modified: Tue, 18 Apr 2023 05:39:57 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f2037c2a933d185399697810bbaa8a464d0ff063b932b21edfcaf641068d6b`  
		Last Modified: Tue, 18 Apr 2023 05:39:57 GMT  
		Size: 7.9 KB (7908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb7c6696693b299c6ca775396a3f776e19489087ceb99fbb661b46714595d73`  
		Last Modified: Tue, 18 Apr 2023 05:39:58 GMT  
		Size: 1.6 MB (1581615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0.0` - linux; arm variant v7

```console
$ docker pull solr@sha256:d87f0589f7c2845e924c43207a651338c16c97d7d6dc4bcec48e5b81333fa40b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317130504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7885b034631769de505cfa7a2c137ed4ca3a1bc14500408f4f79a0b4043f906`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:52:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:52:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:52:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:53:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:53:36 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:54:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:54:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:42:24 GMT
ARG SOLR_VERSION=9.0.0
# Tue, 18 Apr 2023 02:42:24 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Tue, 18 Apr 2023 02:42:24 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Tue, 18 Apr 2023 02:42:24 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:42:24 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:42:24 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 02:42:24 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 02:42:25 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 02:43:12 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 02:43:13 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 02:43:13 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 02:43:14 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 02:43:14 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 02:43:14 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 02:43:14 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 02:43:14 GMT
LABEL org.opencontainers.image.version=9.0.0
# Tue, 18 Apr 2023 02:43:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 02:43:14 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 02:43:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:43:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 02:43:16 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 02:43:20 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 02:43:20 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:43:20 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:43:20 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:43:20 GMT
USER solr
# Tue, 18 Apr 2023 02:43:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:43:20 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85796ae94aa6103041abcc6b06ff12a50d94cadaf6e06eb70a7394c3872a6748`  
		Last Modified: Tue, 18 Apr 2023 01:55:40 GMT  
		Size: 19.5 MB (19465888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cce25c2e3b898f27ed23666a27be2cf47a2d62ace6c9630292dd9db7e2c67a`  
		Last Modified: Tue, 18 Apr 2023 01:56:11 GMT  
		Size: 44.5 MB (44529877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc071ae82a251704f7fd76936abcd7ba3254e014f37f54c2a0e3382398a9027`  
		Last Modified: Tue, 18 Apr 2023 01:56:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729935b9475e1a5c9d749c462c66dc4feeef3ac2ab6eb0b5210a8da556334f9f`  
		Last Modified: Tue, 18 Apr 2023 02:45:25 GMT  
		Size: 227.1 MB (227140646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0d9bcf8720cc8ac9d25548c42d3e312e7bf657a9ae9bb39e70b8b28580cc09`  
		Last Modified: Tue, 18 Apr 2023 02:45:13 GMT  
		Size: 4.2 KB (4225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edb4a37ae5a67ae98b159249438983fda2f9f94121d0f382fe6f8f656554afd`  
		Last Modified: Tue, 18 Apr 2023 02:45:12 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfdabd208deb1701eae64a822800fc6606c1cf3eabe04c7b1fafba629896b05`  
		Last Modified: Tue, 18 Apr 2023 02:45:12 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fbb7c77a9b97e47e625e18d1437411da4080b4ea574e19c01f10dde13d5f1a`  
		Last Modified: Tue, 18 Apr 2023 02:45:13 GMT  
		Size: 1.4 MB (1394613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0.0` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:04b463901ac8bde6a6272968ee59681b13ac42b5fc6f51354aa63e950303c655
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 MB (323539610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7d64830b601b2d2e151a405e707709593e852282532226766335d39e6f8d9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:40:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:40:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:42:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:42:18 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:42:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:42:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 03:20:25 GMT
ARG SOLR_VERSION=9.0.0
# Tue, 18 Apr 2023 03:20:25 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Tue, 18 Apr 2023 03:20:25 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Tue, 18 Apr 2023 03:20:26 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 03:20:26 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 03:20:26 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 03:20:26 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 03:20:26 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 03:21:07 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 03:21:08 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 03:21:08 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 03:21:09 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 03:21:09 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 03:21:09 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 03:21:09 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 03:21:09 GMT
LABEL org.opencontainers.image.version=9.0.0
# Tue, 18 Apr 2023 03:21:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 03:21:09 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 03:21:10 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 03:21:10 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 03:21:11 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 03:21:14 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 03:21:14 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 03:21:14 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 03:21:14 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 03:21:14 GMT
USER solr
# Tue, 18 Apr 2023 03:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 03:21:15 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f855dc454f40dbe47d375c509772787d9d27ff505e14349af4f2e3944f28f75`  
		Last Modified: Tue, 18 Apr 2023 01:44:38 GMT  
		Size: 20.8 MB (20815202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c91968e85b36d056d961163f2b9155edf8119f19516132648c5ecae886bcb3`  
		Last Modified: Tue, 18 Apr 2023 01:45:04 GMT  
		Size: 46.4 MB (46422365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6e32ee26ed47aaac9a5a70c0af73a59858c966aa6646cc3b0151c938bf39b1`  
		Last Modified: Tue, 18 Apr 2023 01:44:58 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0524d79428e8b6d258e182e12c143bc4636644497eb2f713d60bdfc592edcd6`  
		Last Modified: Tue, 18 Apr 2023 03:22:57 GMT  
		Size: 227.6 MB (227649927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02d66c108983824382ae01d655355e198973423b56fe3eac73aee5179245f16`  
		Last Modified: Tue, 18 Apr 2023 03:22:48 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2681b3124697ad3547533a9029d2e44719236d1c5eae31b97c12ac3d5ea9b6`  
		Last Modified: Tue, 18 Apr 2023 03:22:48 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b070826d2cc919b0a9d715e8dc23ac37c6b5068504db8966f7a4ea17da59adf`  
		Last Modified: Tue, 18 Apr 2023 03:22:48 GMT  
		Size: 7.9 KB (7899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c094f24ea3e7d5f503111a9b1379c03432bce9153ceba74dd261b293c853d1f`  
		Last Modified: Tue, 18 Apr 2023 03:22:48 GMT  
		Size: 1.4 MB (1443110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0.0` - linux; ppc64le

```console
$ docker pull solr@sha256:a9475313e73f548e27cdf2bc5e191e9396e588873e85d262d8afcb1355eb5ff2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332285619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f67f099c986d27845fa804471808cfa221c43cd40b3a871d7d61266dc897671`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:06:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:06:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:06:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:09:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:09:19 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:10:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:10:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:34:21 GMT
ARG SOLR_VERSION=9.0.0
# Tue, 18 Apr 2023 02:34:22 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Tue, 18 Apr 2023 02:34:23 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Tue, 18 Apr 2023 02:34:24 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:34:24 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:34:24 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 02:34:25 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 02:34:25 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 02:35:12 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 02:35:15 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 02:35:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 02:35:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 02:35:17 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 02:35:17 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 02:35:17 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 02:35:17 GMT
LABEL org.opencontainers.image.version=9.0.0
# Tue, 18 Apr 2023 02:35:18 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 02:35:18 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 02:35:19 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:35:20 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 02:35:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 02:35:31 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 02:35:31 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:35:31 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:35:32 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:35:32 GMT
USER solr
# Tue, 18 Apr 2023 02:35:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:35:33 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d16c8f7fe3c69e12b82f6ead20825685acccc07c7db20352690c45095874956`  
		Last Modified: Tue, 18 Apr 2023 01:13:05 GMT  
		Size: 22.1 MB (22066207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2766b2ad3fad77d8cd1101de070f2cbc3f36ed8fdef8d95dce041bca895bd1f`  
		Last Modified: Tue, 18 Apr 2023 01:13:48 GMT  
		Size: 46.8 MB (46780913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ba72e32ba8796d6aa8e1b06921ca5c30137cd512ca4f20ca3a6525e2385cd2`  
		Last Modified: Tue, 18 Apr 2023 01:13:36 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4a7787e814f2522f6da4ac6a7d7d6f8d7044671f7a21a0d9367db996a2091e`  
		Last Modified: Tue, 18 Apr 2023 02:38:28 GMT  
		Size: 228.5 MB (228520977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e9f7f73cc13eaa6b8dcc824380daa8713edf23035070230bf611c9852556f`  
		Last Modified: Tue, 18 Apr 2023 02:38:09 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7351a9bd649a1fca781ccf335ec1846158f67665b5c6bea8f4df0981daf1ee`  
		Last Modified: Tue, 18 Apr 2023 02:38:09 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001b4d4b51c19699698e864b870de173145ae13112455690b827d435e3e14707`  
		Last Modified: Tue, 18 Apr 2023 02:38:09 GMT  
		Size: 7.9 KB (7901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2420793c8e6a25c0ea6bf5ae7f54b01e975bcea880317865fecfb8a53a586b`  
		Last Modified: Tue, 18 Apr 2023 02:38:10 GMT  
		Size: 1.6 MB (1603967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0.0` - linux; s390x

```console
$ docker pull solr@sha256:b0b10f10c4b3f0a46e01b9cdd9bbda792ddf06647479c6c57aecc0989f1bd0b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.4 MB (319373122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92814c5d4520c50905c171e10736316604fa13798095d7fa3c5209841b80063`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:16:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:16:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:16:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:17:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:17:10 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:17:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:17:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_VERSION=9.0.0
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 17:04:49 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Tue, 18 Apr 2023 17:05:09 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.version=9.0.0
# Tue, 18 Apr 2023 17:05:13 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 17:05:13 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 17:05:14 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 17:05:14 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 17:05:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 17:05:18 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 17:05:18 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 17:05:18 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 17:05:18 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 17:05:18 GMT
USER solr
# Tue, 18 Apr 2023 17:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 17:05:19 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf6c28f706c8f54c079ff27fe5409527f68c7463df6adf843d835f265547cf5`  
		Last Modified: Tue, 18 Apr 2023 01:19:02 GMT  
		Size: 19.5 MB (19532693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef55f447b7c061c28ebda47f938df25295b85f1e950785fbf350c166ce482a24`  
		Last Modified: Tue, 18 Apr 2023 01:19:26 GMT  
		Size: 43.7 MB (43739777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6627870afe22e0029eee4a5cb3c10c040a070bcd6c443b86248fb66151725bb6`  
		Last Modified: Tue, 18 Apr 2023 01:19:20 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cc4d3f8fcdf8e2799184cf4370edd3318456a1ff69eb195086ae7993030bb6`  
		Last Modified: Tue, 18 Apr 2023 17:06:52 GMT  
		Size: 227.6 MB (227575740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27aea3cbfd9d56f917e11ceff90c24df7e00c872834596a1f8f971385880ef6`  
		Last Modified: Tue, 18 Apr 2023 17:06:41 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e345e4d33bc7de7e08d81012d30f0956b9b1d20037ba6dfe29242ef94ee20`  
		Last Modified: Tue, 18 Apr 2023 17:06:41 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ee5fd9a7f4e529237b057d12170b75ce61ae19bc7f4c60834800e5a7b04202`  
		Last Modified: Tue, 18 Apr 2023 17:06:41 GMT  
		Size: 7.9 KB (7899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb32a39cbc8de15dfbda608e5bd78b87c49719651e5556c9c472b328c9fe535`  
		Last Modified: Tue, 18 Apr 2023 17:06:41 GMT  
		Size: 1.5 MB (1495929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:9.1`

```console
$ docker pull solr@sha256:2ef98d882324beee7a603032ad66c93b8b79232a5c103114a4f5ea314ea421f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:9.1` - linux; amd64

```console
$ docker pull solr@sha256:80658a894fbda0918ddb14af9b4f2802ebe65250c10e41d3e344f7f2b6f4d1f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330947807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c10e05a6a28f30bb535d8f21ea16df798f3d8b9e695324911cbceed695df00e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 00:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 00:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 00:44:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:44:48 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 00:45:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 00:45:16 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 05:34:28 GMT
ARG SOLR_VERSION=9.1.1
# Tue, 18 Apr 2023 05:34:28 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Tue, 18 Apr 2023 05:34:28 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Tue, 18 Apr 2023 05:34:28 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 05:34:28 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 05:34:29 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 05:34:29 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 05:34:29 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 05:36:09 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.version=9.1.1
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 05:36:10 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 05:36:11 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 05:36:11 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 05:36:12 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 05:36:20 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 05:36:20 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 05:36:20 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 05:36:20 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 05:36:20 GMT
USER 8983
# Tue, 18 Apr 2023 05:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 05:36:20 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b493027a1bf3e6a19b932ebe3c6dbfe19dc6a4583dfe39282977a57c89b31e87`  
		Last Modified: Tue, 18 Apr 2023 00:47:39 GMT  
		Size: 20.1 MB (20096839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02938177297ab7e29f7435f1f8092e05942dc412fbdfa6c1421589d8ef0adb57`  
		Last Modified: Tue, 18 Apr 2023 00:48:08 GMT  
		Size: 46.9 MB (46937043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e9595e3a57ad3c2eaf905104408a625b61809733c58a795c86405e275aea0b`  
		Last Modified: Tue, 18 Apr 2023 00:48:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ee77bff8d90cf9a351e1ce423014f4ff0f658293ca052a701886ea666d5fcc`  
		Last Modified: Tue, 18 Apr 2023 05:39:49 GMT  
		Size: 233.7 MB (233740953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5123a34ee6fa079f353e4bc304854acc6ffe3ba9cd2a5bfa47a7d4fda94b88be`  
		Last Modified: Tue, 18 Apr 2023 05:39:38 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dfda3f43afacbf8f2eb91877ce1c0f090c255c372e5a4f2022c017dad3ccfd`  
		Last Modified: Tue, 18 Apr 2023 05:39:39 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d1f2ce2a1c23a9482d1aacca94ff05f266b538c1dd86725e930e309ad625f`  
		Last Modified: Tue, 18 Apr 2023 05:39:38 GMT  
		Size: 8.1 KB (8085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a342ac0282ccec59096fc2e74be5d78fde3c37f3ff8efe643a91945f37386448`  
		Last Modified: Tue, 18 Apr 2023 05:39:39 GMT  
		Size: 1.6 MB (1581649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1` - linux; arm variant v7

```console
$ docker pull solr@sha256:e6bf5a7aa3acf9af92dd1daa8a39542796e075358e6359a6d59ef5126d029ef6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323210806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cba3d529bc528ab942d2e0944b8fced1d86b2756f99fe9b0d8fcca7ca38d719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:52:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:52:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:52:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:53:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:53:36 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:54:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:54:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:41:15 GMT
ARG SOLR_VERSION=9.1.1
# Tue, 18 Apr 2023 02:41:15 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Tue, 18 Apr 2023 02:41:16 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Tue, 18 Apr 2023 02:41:16 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:41:16 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:41:16 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 02:41:16 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 02:41:16 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 02:42:01 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.version=9.1.1
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 02:42:03 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 02:42:04 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:42:04 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 02:42:05 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 02:42:12 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 02:42:12 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:42:12 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:42:12 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:42:12 GMT
USER 8983
# Tue, 18 Apr 2023 02:42:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:42:13 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85796ae94aa6103041abcc6b06ff12a50d94cadaf6e06eb70a7394c3872a6748`  
		Last Modified: Tue, 18 Apr 2023 01:55:40 GMT  
		Size: 19.5 MB (19465888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cce25c2e3b898f27ed23666a27be2cf47a2d62ace6c9630292dd9db7e2c67a`  
		Last Modified: Tue, 18 Apr 2023 01:56:11 GMT  
		Size: 44.5 MB (44529877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc071ae82a251704f7fd76936abcd7ba3254e014f37f54c2a0e3382398a9027`  
		Last Modified: Tue, 18 Apr 2023 01:56:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d131fa5c0427db0079655aa5ef576b6abe10a278db210defc6f55e938327e52f`  
		Last Modified: Tue, 18 Apr 2023 02:45:04 GMT  
		Size: 233.2 MB (233220697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95bcd54e79b130871436f8ed209655896d56a7200f297d4254924ec975501a0`  
		Last Modified: Tue, 18 Apr 2023 02:44:52 GMT  
		Size: 4.2 KB (4227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bc6b47cde69c048851e1aa0b623ac96150c5129cc90acab15ba971c6a3f957`  
		Last Modified: Tue, 18 Apr 2023 02:44:51 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1658899e1e94a34e7665d14e7e4a1e0640891734558498b18e5c3a651576d32`  
		Last Modified: Tue, 18 Apr 2023 02:44:51 GMT  
		Size: 8.1 KB (8086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101dd1bc9a89d85ebb898a833ee703cb9a197b20e0d6281374379a60814431de`  
		Last Modified: Tue, 18 Apr 2023 02:44:52 GMT  
		Size: 1.4 MB (1394678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:756183ae377d29f4285ffc3ecae5dfbbb5a3ababadb28b12166dd36ddf186549
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329621218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a7971549dffa1c9364de4726369f6ebf901d6487248614fe8098b27873a4ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:40:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:40:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:42:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:42:18 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:42:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:42:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 03:19:28 GMT
ARG SOLR_VERSION=9.1.1
# Tue, 18 Apr 2023 03:19:28 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Tue, 18 Apr 2023 03:19:28 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Tue, 18 Apr 2023 03:19:28 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 03:19:28 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 03:19:28 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 03:19:29 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 03:19:29 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 03:20:08 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.version=9.1.1
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 03:20:10 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 03:20:11 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 03:20:11 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 03:20:12 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 03:20:19 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 03:20:19 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 03:20:19 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 03:20:20 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 03:20:20 GMT
USER 8983
# Tue, 18 Apr 2023 03:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 03:20:20 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f855dc454f40dbe47d375c509772787d9d27ff505e14349af4f2e3944f28f75`  
		Last Modified: Tue, 18 Apr 2023 01:44:38 GMT  
		Size: 20.8 MB (20815202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c91968e85b36d056d961163f2b9155edf8119f19516132648c5ecae886bcb3`  
		Last Modified: Tue, 18 Apr 2023 01:45:04 GMT  
		Size: 46.4 MB (46422365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6e32ee26ed47aaac9a5a70c0af73a59858c966aa6646cc3b0151c938bf39b1`  
		Last Modified: Tue, 18 Apr 2023 01:44:58 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89355900f95b0a212d969f16b350857c1f2c484164a03a38942d9852b91faa46`  
		Last Modified: Tue, 18 Apr 2023 03:22:40 GMT  
		Size: 233.7 MB (233731364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5d238c8959564a4b0cdc672895e60492cdc82ad83c5d830b141bd5ff5fec7b`  
		Last Modified: Tue, 18 Apr 2023 03:22:31 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797cde12c943c3478e869d8f23de31c7a29b17971f1b3a7162c2bb3ea213ecc5`  
		Last Modified: Tue, 18 Apr 2023 03:22:31 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5c3e86e33823bf7401a4a0e404d76113f801a1114b2c24a1d9b3e50af3fdcb`  
		Last Modified: Tue, 18 Apr 2023 03:22:31 GMT  
		Size: 8.1 KB (8085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e485d8d417dab6f7edacf648b1b41ec329e3a9cc83e99f106c73681d92dc29`  
		Last Modified: Tue, 18 Apr 2023 03:22:31 GMT  
		Size: 1.4 MB (1443095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1` - linux; ppc64le

```console
$ docker pull solr@sha256:3c5097ba33684f4bdb8258bd26d85303724f6ce81bb5f54c4aea1a15c4585303
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338365814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f5bb8dc757b472f4c62e63a921b120da809233cb9190aa15bebfaffcba87c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:06:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:06:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:06:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:09:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:09:19 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:10:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:10:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:32:42 GMT
ARG SOLR_VERSION=9.1.1
# Tue, 18 Apr 2023 02:32:43 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Tue, 18 Apr 2023 02:32:45 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Tue, 18 Apr 2023 02:32:45 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:32:46 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:32:46 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 02:32:48 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 02:32:48 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 02:33:41 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 02:33:46 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 02:33:46 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 02:33:47 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 02:33:47 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 02:33:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 02:33:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 02:33:49 GMT
LABEL org.opencontainers.image.version=9.1.1
# Tue, 18 Apr 2023 02:33:49 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 02:33:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 02:33:51 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:33:54 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 02:33:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 02:34:10 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 02:34:10 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:34:11 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:34:12 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:34:13 GMT
USER 8983
# Tue, 18 Apr 2023 02:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:34:14 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d16c8f7fe3c69e12b82f6ead20825685acccc07c7db20352690c45095874956`  
		Last Modified: Tue, 18 Apr 2023 01:13:05 GMT  
		Size: 22.1 MB (22066207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2766b2ad3fad77d8cd1101de070f2cbc3f36ed8fdef8d95dce041bca895bd1f`  
		Last Modified: Tue, 18 Apr 2023 01:13:48 GMT  
		Size: 46.8 MB (46780913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ba72e32ba8796d6aa8e1b06921ca5c30137cd512ca4f20ca3a6525e2385cd2`  
		Last Modified: Tue, 18 Apr 2023 01:13:36 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302e16b6fd181f6fdc5ede457bede1e63c3b6d468eb5d28a6d92a10f3878cd8f`  
		Last Modified: Tue, 18 Apr 2023 02:37:59 GMT  
		Size: 234.6 MB (234600949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81ec90eab47bad80aa5e4e9859f172205ee0093518e1302f0340d16a6180558`  
		Last Modified: Tue, 18 Apr 2023 02:37:22 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e981102c55e3c8d3d16d27f35b0c277eb243cd8a45f979cfa7c32c36e6b54d1`  
		Last Modified: Tue, 18 Apr 2023 02:37:23 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf068fed518dd04af11721ec849a2937fab5f7ededfe45f4ba601794b6574df`  
		Last Modified: Tue, 18 Apr 2023 02:37:22 GMT  
		Size: 8.1 KB (8095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec38ee91a72425eb130aaccb73777aa1b6c943ce624c863994655ee9c4307d6`  
		Last Modified: Tue, 18 Apr 2023 02:37:23 GMT  
		Size: 1.6 MB (1603996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1` - linux; s390x

```console
$ docker pull solr@sha256:3616c30b842f812db2edf7452fddb29180163312486314dc8f23994faa69b6f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325454877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3771a7e2fdd602fa4066fea2fc9d6d0c4697194b3ce7475618d3cc3ec2eed4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:16:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:16:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:16:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:17:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:17:10 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:17:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:17:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 17:04:07 GMT
ARG SOLR_VERSION=9.1.1
# Tue, 18 Apr 2023 17:04:07 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Tue, 18 Apr 2023 17:04:07 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Tue, 18 Apr 2023 17:04:07 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 17:04:07 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 17:04:07 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 17:04:08 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 17:04:08 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 17:04:32 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 17:04:35 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 17:04:35 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 17:04:36 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 17:04:36 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 17:04:36 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 17:04:36 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 17:04:36 GMT
LABEL org.opencontainers.image.version=9.1.1
# Tue, 18 Apr 2023 17:04:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 17:04:36 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 17:04:37 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 17:04:37 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 17:04:37 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 17:04:42 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 17:04:42 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 17:04:42 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 17:04:42 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 17:04:42 GMT
USER 8983
# Tue, 18 Apr 2023 17:04:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 17:04:43 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf6c28f706c8f54c079ff27fe5409527f68c7463df6adf843d835f265547cf5`  
		Last Modified: Tue, 18 Apr 2023 01:19:02 GMT  
		Size: 19.5 MB (19532693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef55f447b7c061c28ebda47f938df25295b85f1e950785fbf350c166ce482a24`  
		Last Modified: Tue, 18 Apr 2023 01:19:26 GMT  
		Size: 43.7 MB (43739777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6627870afe22e0029eee4a5cb3c10c040a070bcd6c443b86248fb66151725bb6`  
		Last Modified: Tue, 18 Apr 2023 01:19:20 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04c3c937c903f511cba6c911fcac432ec34f273b671f4f3a9b4ca9d00f1788d`  
		Last Modified: Tue, 18 Apr 2023 17:06:35 GMT  
		Size: 233.7 MB (233657290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3773c3d8097ab2350bc95c0f299b2b78dc1abaae98b5faab2896ce8c68434353`  
		Last Modified: Tue, 18 Apr 2023 17:06:23 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e58d908024feecd566f694c0ad3db90907d9dc454ea4478df16d2a3a4a1d695`  
		Last Modified: Tue, 18 Apr 2023 17:06:23 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf24e6e195513455dc42108d38d00ee5ab8d7ae490fcdf445db1592b015cfcc`  
		Last Modified: Tue, 18 Apr 2023 17:06:23 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd9b9748035a5e990830a5dd57e3c97747a70f0daed7042490aa81cc08a78ec`  
		Last Modified: Tue, 18 Apr 2023 17:06:24 GMT  
		Size: 1.5 MB (1495951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:9.1.1`

```console
$ docker pull solr@sha256:2ef98d882324beee7a603032ad66c93b8b79232a5c103114a4f5ea314ea421f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:9.1.1` - linux; amd64

```console
$ docker pull solr@sha256:80658a894fbda0918ddb14af9b4f2802ebe65250c10e41d3e344f7f2b6f4d1f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330947807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c10e05a6a28f30bb535d8f21ea16df798f3d8b9e695324911cbceed695df00e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:05:13 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:05:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:05:13 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:05:15 GMT
ADD file:d05d1c0936b046937bd5755876db2f8da3ed8ccbcf464bb56c312fbc7ed78589 in / 
# Thu, 13 Apr 2023 13:05:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 00:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 00:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 00:44:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:44:48 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 00:45:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 00:45:16 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 05:34:28 GMT
ARG SOLR_VERSION=9.1.1
# Tue, 18 Apr 2023 05:34:28 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Tue, 18 Apr 2023 05:34:28 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Tue, 18 Apr 2023 05:34:28 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 05:34:28 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 05:34:29 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 05:34:29 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 05:34:29 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 05:36:09 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.version=9.1.1
# Tue, 18 Apr 2023 05:36:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 05:36:10 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 05:36:11 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 05:36:11 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 05:36:12 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 05:36:20 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 05:36:20 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 05:36:20 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 05:36:20 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 05:36:20 GMT
USER 8983
# Tue, 18 Apr 2023 05:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 05:36:20 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:99803d4b97f3db529ae9ca4174b0951afac6b309e7deaa8ec3214c584e02b3a8`  
		Last Modified: Thu, 13 Apr 2023 03:03:13 GMT  
		Size: 28.6 MB (28578563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b493027a1bf3e6a19b932ebe3c6dbfe19dc6a4583dfe39282977a57c89b31e87`  
		Last Modified: Tue, 18 Apr 2023 00:47:39 GMT  
		Size: 20.1 MB (20096839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02938177297ab7e29f7435f1f8092e05942dc412fbdfa6c1421589d8ef0adb57`  
		Last Modified: Tue, 18 Apr 2023 00:48:08 GMT  
		Size: 46.9 MB (46937043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e9595e3a57ad3c2eaf905104408a625b61809733c58a795c86405e275aea0b`  
		Last Modified: Tue, 18 Apr 2023 00:48:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ee77bff8d90cf9a351e1ce423014f4ff0f658293ca052a701886ea666d5fcc`  
		Last Modified: Tue, 18 Apr 2023 05:39:49 GMT  
		Size: 233.7 MB (233740953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5123a34ee6fa079f353e4bc304854acc6ffe3ba9cd2a5bfa47a7d4fda94b88be`  
		Last Modified: Tue, 18 Apr 2023 05:39:38 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dfda3f43afacbf8f2eb91877ce1c0f090c255c372e5a4f2022c017dad3ccfd`  
		Last Modified: Tue, 18 Apr 2023 05:39:39 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d1f2ce2a1c23a9482d1aacca94ff05f266b538c1dd86725e930e309ad625f`  
		Last Modified: Tue, 18 Apr 2023 05:39:38 GMT  
		Size: 8.1 KB (8085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a342ac0282ccec59096fc2e74be5d78fde3c37f3ff8efe643a91945f37386448`  
		Last Modified: Tue, 18 Apr 2023 05:39:39 GMT  
		Size: 1.6 MB (1581649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1.1` - linux; arm variant v7

```console
$ docker pull solr@sha256:e6bf5a7aa3acf9af92dd1daa8a39542796e075358e6359a6d59ef5126d029ef6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323210806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cba3d529bc528ab942d2e0944b8fced1d86b2756f99fe9b0d8fcca7ca38d719`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:47 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:48 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:20:50 GMT
ADD file:0da456bd328984fcedf5367b46a38da6ca4b43061baf6d1283380962cddc7481 in / 
# Thu, 13 Apr 2023 13:20:50 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:52:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:52:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:52:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:53:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:53:36 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:54:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:54:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:41:15 GMT
ARG SOLR_VERSION=9.1.1
# Tue, 18 Apr 2023 02:41:15 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Tue, 18 Apr 2023 02:41:16 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Tue, 18 Apr 2023 02:41:16 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:41:16 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:41:16 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 02:41:16 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 02:41:16 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 02:42:01 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.version=9.1.1
# Tue, 18 Apr 2023 02:42:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 02:42:03 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 02:42:04 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:42:04 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 02:42:05 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 02:42:12 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 02:42:12 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:42:12 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:42:12 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:42:12 GMT
USER 8983
# Tue, 18 Apr 2023 02:42:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:42:13 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e68c91cb250f35160f683afa80c3ada46f06948ded46a188be490ea3afff08f5`  
		Last Modified: Fri, 14 Apr 2023 09:34:28 GMT  
		Size: 24.6 MB (24586976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85796ae94aa6103041abcc6b06ff12a50d94cadaf6e06eb70a7394c3872a6748`  
		Last Modified: Tue, 18 Apr 2023 01:55:40 GMT  
		Size: 19.5 MB (19465888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cce25c2e3b898f27ed23666a27be2cf47a2d62ace6c9630292dd9db7e2c67a`  
		Last Modified: Tue, 18 Apr 2023 01:56:11 GMT  
		Size: 44.5 MB (44529877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc071ae82a251704f7fd76936abcd7ba3254e014f37f54c2a0e3382398a9027`  
		Last Modified: Tue, 18 Apr 2023 01:56:04 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d131fa5c0427db0079655aa5ef576b6abe10a278db210defc6f55e938327e52f`  
		Last Modified: Tue, 18 Apr 2023 02:45:04 GMT  
		Size: 233.2 MB (233220697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95bcd54e79b130871436f8ed209655896d56a7200f297d4254924ec975501a0`  
		Last Modified: Tue, 18 Apr 2023 02:44:52 GMT  
		Size: 4.2 KB (4227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bc6b47cde69c048851e1aa0b623ac96150c5129cc90acab15ba971c6a3f957`  
		Last Modified: Tue, 18 Apr 2023 02:44:51 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1658899e1e94a34e7665d14e7e4a1e0640891734558498b18e5c3a651576d32`  
		Last Modified: Tue, 18 Apr 2023 02:44:51 GMT  
		Size: 8.1 KB (8086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101dd1bc9a89d85ebb898a833ee703cb9a197b20e0d6281374379a60814431de`  
		Last Modified: Tue, 18 Apr 2023 02:44:52 GMT  
		Size: 1.4 MB (1394678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1.1` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:756183ae377d29f4285ffc3ecae5dfbbb5a3ababadb28b12166dd36ddf186549
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329621218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a7971549dffa1c9364de4726369f6ebf901d6487248614fe8098b27873a4ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:50 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:59 GMT
ADD file:0150fa02321f8be160e90ff64583d263fe651b5d418ab65f05ba604449ab47c6 in / 
# Thu, 13 Apr 2023 13:10:00 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:40:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:40:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:42:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:42:18 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:42:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:42:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 03:19:28 GMT
ARG SOLR_VERSION=9.1.1
# Tue, 18 Apr 2023 03:19:28 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Tue, 18 Apr 2023 03:19:28 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Tue, 18 Apr 2023 03:19:28 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 03:19:28 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 03:19:28 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 03:19:29 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 03:19:29 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 03:20:08 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.version=9.1.1
# Tue, 18 Apr 2023 03:20:10 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 03:20:10 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 03:20:11 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 03:20:11 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 03:20:12 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 03:20:19 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 03:20:19 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 03:20:19 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 03:20:20 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 03:20:20 GMT
USER 8983
# Tue, 18 Apr 2023 03:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 03:20:20 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2378679266ac5157323158b6e52e7a884e559db5217037e57992e47a1667d525`  
		Last Modified: Fri, 14 Apr 2023 07:39:20 GMT  
		Size: 27.2 MB (27196396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f855dc454f40dbe47d375c509772787d9d27ff505e14349af4f2e3944f28f75`  
		Last Modified: Tue, 18 Apr 2023 01:44:38 GMT  
		Size: 20.8 MB (20815202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c91968e85b36d056d961163f2b9155edf8119f19516132648c5ecae886bcb3`  
		Last Modified: Tue, 18 Apr 2023 01:45:04 GMT  
		Size: 46.4 MB (46422365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6e32ee26ed47aaac9a5a70c0af73a59858c966aa6646cc3b0151c938bf39b1`  
		Last Modified: Tue, 18 Apr 2023 01:44:58 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89355900f95b0a212d969f16b350857c1f2c484164a03a38942d9852b91faa46`  
		Last Modified: Tue, 18 Apr 2023 03:22:40 GMT  
		Size: 233.7 MB (233731364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5d238c8959564a4b0cdc672895e60492cdc82ad83c5d830b141bd5ff5fec7b`  
		Last Modified: Tue, 18 Apr 2023 03:22:31 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797cde12c943c3478e869d8f23de31c7a29b17971f1b3a7162c2bb3ea213ecc5`  
		Last Modified: Tue, 18 Apr 2023 03:22:31 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5c3e86e33823bf7401a4a0e404d76113f801a1114b2c24a1d9b3e50af3fdcb`  
		Last Modified: Tue, 18 Apr 2023 03:22:31 GMT  
		Size: 8.1 KB (8085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e485d8d417dab6f7edacf648b1b41ec329e3a9cc83e99f106c73681d92dc29`  
		Last Modified: Tue, 18 Apr 2023 03:22:31 GMT  
		Size: 1.4 MB (1443095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1.1` - linux; ppc64le

```console
$ docker pull solr@sha256:3c5097ba33684f4bdb8258bd26d85303724f6ce81bb5f54c4aea1a15c4585303
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338365814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f5bb8dc757b472f4c62e63a921b120da809233cb9190aa15bebfaffcba87c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:36 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:37 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:40 GMT
ADD file:faba3891f58656ec753ba6ca4b63e7c1f27bcd236b665634b05d5bc1b1ceee0a in / 
# Thu, 13 Apr 2023 13:09:40 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:06:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:06:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:06:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:09:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:09:19 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:10:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:10:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 02:32:42 GMT
ARG SOLR_VERSION=9.1.1
# Tue, 18 Apr 2023 02:32:43 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Tue, 18 Apr 2023 02:32:45 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Tue, 18 Apr 2023 02:32:45 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 02:32:46 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 02:32:46 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 02:32:48 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 02:32:48 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 02:33:41 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 02:33:46 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 02:33:46 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 02:33:47 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 02:33:47 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 02:33:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 02:33:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 02:33:49 GMT
LABEL org.opencontainers.image.version=9.1.1
# Tue, 18 Apr 2023 02:33:49 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 02:33:50 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 02:33:51 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 02:33:54 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 02:33:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 02:34:10 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 02:34:10 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 02:34:11 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 02:34:12 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 02:34:13 GMT
USER 8983
# Tue, 18 Apr 2023 02:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 02:34:14 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d276072145993a42aed3e2b3e8cd26b6e08aab266d9c9d792ee89b26150681da`  
		Last Modified: Fri, 14 Apr 2023 09:36:00 GMT  
		Size: 33.3 MB (33300980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d16c8f7fe3c69e12b82f6ead20825685acccc07c7db20352690c45095874956`  
		Last Modified: Tue, 18 Apr 2023 01:13:05 GMT  
		Size: 22.1 MB (22066207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2766b2ad3fad77d8cd1101de070f2cbc3f36ed8fdef8d95dce041bca895bd1f`  
		Last Modified: Tue, 18 Apr 2023 01:13:48 GMT  
		Size: 46.8 MB (46780913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ba72e32ba8796d6aa8e1b06921ca5c30137cd512ca4f20ca3a6525e2385cd2`  
		Last Modified: Tue, 18 Apr 2023 01:13:36 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302e16b6fd181f6fdc5ede457bede1e63c3b6d468eb5d28a6d92a10f3878cd8f`  
		Last Modified: Tue, 18 Apr 2023 02:37:59 GMT  
		Size: 234.6 MB (234600949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81ec90eab47bad80aa5e4e9859f172205ee0093518e1302f0340d16a6180558`  
		Last Modified: Tue, 18 Apr 2023 02:37:22 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e981102c55e3c8d3d16d27f35b0c277eb243cd8a45f979cfa7c32c36e6b54d1`  
		Last Modified: Tue, 18 Apr 2023 02:37:23 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf068fed518dd04af11721ec849a2937fab5f7ededfe45f4ba601794b6574df`  
		Last Modified: Tue, 18 Apr 2023 02:37:22 GMT  
		Size: 8.1 KB (8095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec38ee91a72425eb130aaccb73777aa1b6c943ce624c863994655ee9c4307d6`  
		Last Modified: Tue, 18 Apr 2023 02:37:23 GMT  
		Size: 1.6 MB (1603996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1.1` - linux; s390x

```console
$ docker pull solr@sha256:3616c30b842f812db2edf7452fddb29180163312486314dc8f23994faa69b6f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325454877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3771a7e2fdd602fa4066fea2fc9d6d0c4697194b3ce7475618d3cc3ec2eed4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:35 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:35 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 13 Apr 2023 13:09:37 GMT
ADD file:44c66c03ba0afcc05de1b2078f83e8bfe04706b31491fcd3fdd93cfc88d5f06c in / 
# Thu, 13 Apr 2023 13:09:37 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:16:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Apr 2023 01:16:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Apr 2023 01:16:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 18 Apr 2023 01:17:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:17:10 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Tue, 18 Apr 2023 01:17:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 18 Apr 2023 01:17:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 18 Apr 2023 17:04:07 GMT
ARG SOLR_VERSION=9.1.1
# Tue, 18 Apr 2023 17:04:07 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Tue, 18 Apr 2023 17:04:07 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Tue, 18 Apr 2023 17:04:07 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 18 Apr 2023 17:04:07 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 18 Apr 2023 17:04:07 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 17:04:08 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 17:04:08 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Tue, 18 Apr 2023 17:04:32 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Tue, 18 Apr 2023 17:04:35 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 18 Apr 2023 17:04:35 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 18 Apr 2023 17:04:36 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 18 Apr 2023 17:04:36 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 18 Apr 2023 17:04:36 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 18 Apr 2023 17:04:36 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 18 Apr 2023 17:04:36 GMT
LABEL org.opencontainers.image.version=9.1.1
# Tue, 18 Apr 2023 17:04:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 18 Apr 2023 17:04:36 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Tue, 18 Apr 2023 17:04:37 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 18 Apr 2023 17:04:37 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Tue, 18 Apr 2023 17:04:37 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Tue, 18 Apr 2023 17:04:42 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Tue, 18 Apr 2023 17:04:42 GMT
VOLUME [/var/solr]
# Tue, 18 Apr 2023 17:04:42 GMT
EXPOSE 8983
# Tue, 18 Apr 2023 17:04:42 GMT
WORKDIR /opt/solr
# Tue, 18 Apr 2023 17:04:42 GMT
USER 8983
# Tue, 18 Apr 2023 17:04:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Apr 2023 17:04:43 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f11b609b1d63f2d37c0e3789823e7a7e62a078bddca7c46da8602655989c62d9`  
		Last Modified: Fri, 14 Apr 2023 09:38:39 GMT  
		Size: 27.0 MB (27016370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf6c28f706c8f54c079ff27fe5409527f68c7463df6adf843d835f265547cf5`  
		Last Modified: Tue, 18 Apr 2023 01:19:02 GMT  
		Size: 19.5 MB (19532693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef55f447b7c061c28ebda47f938df25295b85f1e950785fbf350c166ce482a24`  
		Last Modified: Tue, 18 Apr 2023 01:19:26 GMT  
		Size: 43.7 MB (43739777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6627870afe22e0029eee4a5cb3c10c040a070bcd6c443b86248fb66151725bb6`  
		Last Modified: Tue, 18 Apr 2023 01:19:20 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04c3c937c903f511cba6c911fcac432ec34f273b671f4f3a9b4ca9d00f1788d`  
		Last Modified: Tue, 18 Apr 2023 17:06:35 GMT  
		Size: 233.7 MB (233657290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3773c3d8097ab2350bc95c0f299b2b78dc1abaae98b5faab2896ce8c68434353`  
		Last Modified: Tue, 18 Apr 2023 17:06:23 GMT  
		Size: 4.3 KB (4332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e58d908024feecd566f694c0ad3db90907d9dc454ea4478df16d2a3a4a1d695`  
		Last Modified: Tue, 18 Apr 2023 17:06:23 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf24e6e195513455dc42108d38d00ee5ab8d7ae490fcdf445db1592b015cfcc`  
		Last Modified: Tue, 18 Apr 2023 17:06:23 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd9b9748035a5e990830a5dd57e3c97747a70f0daed7042490aa81cc08a78ec`  
		Last Modified: Tue, 18 Apr 2023 17:06:24 GMT  
		Size: 1.5 MB (1495951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:9.2`

```console
$ docker pull solr@sha256:6a63019e5694591e2d1c53d56cdcba819235adbd1e85d91f0f82cc7562ea1ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:9.2` - linux; amd64

```console
$ docker pull solr@sha256:cbee52e4b6a1e30d450e8ca19402c3bc15d4d8e8a75ca8501cb0f7f642cc76ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.9 MB (374859971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d43c32e8ee6e715af99f55ba48e134125af6eadbc175932523f25a1070ce4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:44:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:46:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:46:48 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:47:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:47:22 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:07 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:52 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:20:53 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:20:54 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:20:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:20:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:21:03 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:21:03 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:21:03 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:21:03 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:21:04 GMT
USER 8983
# Fri, 24 Mar 2023 20:21:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:21:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182a611d05b01879f065473c49fb968b8d30312f931350ea07af1c46aa8b4f9`  
		Last Modified: Thu, 16 Mar 2023 02:53:08 GMT  
		Size: 17.0 MB (16975402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb51f9f63778bb9fb97f2cb054b54dfc5098aba2931664a12930c35cf464ca6`  
		Last Modified: Thu, 16 Mar 2023 02:54:00 GMT  
		Size: 46.9 MB (46935467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1365afd8cae0153f1c2bfcf8a4c9b78f2e6e0f18431b0460c63c1fede7507fee`  
		Last Modified: Thu, 16 Mar 2023 02:53:53 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b70190cd6e82c4ac613c9f0f9bf4e42155528b445617672bcd7a211b2a2104`  
		Last Modified: Fri, 24 Mar 2023 20:21:43 GMT  
		Size: 278.7 MB (278678830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c984f04f09ad32d618a63f426eb4127534ca414910aa8b56da2355a3bcf17c17`  
		Last Modified: Fri, 24 Mar 2023 20:21:31 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888b9068f218433d417da0cd83cca3863ad2cbea9bab37c09fc52a63fab6206e`  
		Last Modified: Fri, 24 Mar 2023 20:21:31 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1599d0444630b3ac11f8d61742ff79acaaec1b9cfcca5e176b131ef54c22bd`  
		Last Modified: Fri, 24 Mar 2023 20:21:32 GMT  
		Size: 8.3 KB (8264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbc52fa8b34cbd17b27c7c562e83344a928724a395e74a740d6bcfbd0aca1e8`  
		Last Modified: Fri, 24 Mar 2023 20:21:32 GMT  
		Size: 1.8 MB (1827370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.2` - linux; arm variant v7

```console
$ docker pull solr@sha256:7ce35f5dfe8a54b79e4886b38ee7bbae1768c5080b38dd88007711f1a730ca97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.0 MB (368994236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0c33c02e827728f7408559ce07896fbcd7ef42a58bd47bd0c340d122ef7c70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:46:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:46:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:46:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:49:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:49:36 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:50:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:50:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 21:14:57 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 21:14:57 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:15:46 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 21:15:48 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 21:15:49 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 21:15:49 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 21:15:50 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 21:15:59 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 21:16:00 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 21:16:00 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 21:16:00 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 21:16:00 GMT
USER 8983
# Fri, 24 Mar 2023 21:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 21:16:00 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:cba1fa3bcdf4f746dcf5b8f86874cee4a6eff75dd5c5cd29e4c912574b12a1c6`  
		Last Modified: Thu, 09 Mar 2023 04:41:14 GMT  
		Size: 27.0 MB (27025397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85169cff2ee4bc04fcfaf94a937435e69eb27ca38bf1dcbd04593cccacf0d702`  
		Last Modified: Thu, 16 Mar 2023 02:56:32 GMT  
		Size: 17.1 MB (17093778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be72bd479c96978965e7a3ad3512673e6ca3b26714713ca967a807e2c0bcdb7e`  
		Last Modified: Thu, 16 Mar 2023 02:57:28 GMT  
		Size: 44.5 MB (44528811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5725cdfe807b737e733d3d3a443ffd37aef0141ba7a33fb98b334c479486085`  
		Last Modified: Thu, 16 Mar 2023 02:57:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f40c0125b4d5835619a97a6e8aa526c71d7c68b45f248b530ebb09d2d1570c6`  
		Last Modified: Fri, 24 Mar 2023 21:16:36 GMT  
		Size: 278.7 MB (278680032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c884c5595959c80781c31e89baa334da69c61145587cecf73ae8777f044fbb01`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 4.2 KB (4224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387e1ea0fbb6ae2834c227fdf0661b61a1dbe74918fddc3fb294bb4dbbbce8b9`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4b5c915fbddf45760ab4310f38f8bce027f6be8d21539defc6c49238e0d1d9`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 8.3 KB (8259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c5e2d209b82002244ea91d52f9d395d4e38adde0830ca8a1a014fd6a0fb50b`  
		Last Modified: Fri, 24 Mar 2023 21:16:21 GMT  
		Size: 1.7 MB (1653357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.2` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:58619b9500a6637702a27985f2cf8b17cb13dae6c2673f3abaa9a1bd824277ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.6 MB (373587696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f72e1df4e02c02f553d7d54dd64951829dbdd59095775a6634ddce70eadc8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:52:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:52:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:52:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:55:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:55:04 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:55:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:55:30 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:47:31 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:47:31 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:48:14 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:48:17 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:48:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:48:17 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:48:17 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:48:18 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:48:18 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:48:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:48:27 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:48:27 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:48:27 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:48:28 GMT
USER 8983
# Fri, 24 Mar 2023 20:48:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:48:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40b70fd7935308ad0e072e7e06ec8c3abdc59beae70ca716dcd04e971680865`  
		Last Modified: Thu, 16 Mar 2023 02:00:42 GMT  
		Size: 18.4 MB (18400790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33dd5efa5ce73b25dc0236fcd408527b63e42c87e6da9672a356731004b8949`  
		Last Modified: Thu, 16 Mar 2023 02:01:25 GMT  
		Size: 46.4 MB (46421360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ce9280353ea6c4511dc5378e2f0f4742d499bf6df15c8d10804513c8c5115a`  
		Last Modified: Thu, 16 Mar 2023 02:01:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab85ed965ce21582560c60a815ae59ae9cf0fcb5c9270ba02dfc5ca1c135b44f`  
		Last Modified: Fri, 24 Mar 2023 20:49:04 GMT  
		Size: 278.7 MB (278678702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47faea25001b6a9178cab60304409e81d636878232dda7e76d519e7490bbc9`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7792e9b554723df7cdd9593ee715d8fe16cfec71a28c58e0b01e2534e7f2c8`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9435de9f76e1e09e2078c456e20cd6a83a757671ecc43398fed205b323cb3c6b`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 8.3 KB (8261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fc7a7f4116bfd1b88180e25c33fa7c4d571df7caad6ffebbec7786b32b2738`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 1.7 MB (1686320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.2` - linux; ppc64le

```console
$ docker pull solr@sha256:f10e0c22e5adec6e85249f7eac5f7a5f930872dbd32a9cd7c770ec7ab6077b61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.3 MB (381276492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08713b2a6558c371eb5008de184f2ae763ef7c3a322e2d740c9665f599eb2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:57:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 03:57:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 03:57:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 04:03:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:03:28 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 04:04:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 04:04:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:16:55 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:18:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:18:18 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:18:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:18:21 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:18:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:18:24 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:18:25 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:18:40 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:18:41 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:18:41 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:18:41 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:18:41 GMT
USER 8983
# Fri, 24 Mar 2023 20:18:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:18:42 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c06c33e4689e5957d961321ac18da32bea369d2eccc9173c9ad8b517f802ea`  
		Last Modified: Thu, 16 Mar 2023 04:14:09 GMT  
		Size: 18.3 MB (18257665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75be9792a67101a27b125eb6a0e465b760b4302cd2fbf3cf19338303bcfe803`  
		Last Modified: Thu, 16 Mar 2023 04:15:24 GMT  
		Size: 46.8 MB (46780948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba3f99059088b7aca45113a2e84d92786ffffd7b3920e17bc78082f1ca41023`  
		Last Modified: Thu, 16 Mar 2023 04:15:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a80e5b79ed57a03fbca62529db243f85c92ae5df2321c4e9f1224711e54a0d8`  
		Last Modified: Fri, 24 Mar 2023 20:19:29 GMT  
		Size: 278.7 MB (278679501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a83b0eea3048a8cc5ee14c0ed706cd75212e6513827c6e50ee8514b3a37ffa`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfda90d0edd877ecc2717bf59c6b25f8810ed05202ab28ba588f60de2cc3332e`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffae90319602b89f29babd93a389ad3dcb0acd2637266cdb4f1e0e4b02309a2`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 8.3 KB (8264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7a5d7ac7a4e26a6795ad596e099b124de0249d7a8cd31eff56a0786195d720`  
		Last Modified: Fri, 24 Mar 2023 20:19:07 GMT  
		Size: 1.8 MB (1833711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.2` - linux; s390x

```console
$ docker pull solr@sha256:55d3908647c17e61e6cc73ac71deba6d9ab2a161bd4aa7b6ea15c7a7a75fab5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369606057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1685dca8b24c2c5e320e5a7ef4c2bb2431ea293974475f5458fee07495a73e61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:06:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:06:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:06:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:07:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:07:59 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:08:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:08:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:42:43 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:43:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:43:20 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:43:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:43:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:43:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:43:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:43:27 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:43:27 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:43:27 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:43:28 GMT
USER 8983
# Fri, 24 Mar 2023 20:43:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:43:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2c7366af510b72cc0b3456fb93cfa0bfc76f7d383db5cb315967e7b1ce2e0c42`  
		Last Modified: Thu, 16 Mar 2023 02:02:40 GMT  
		Size: 28.6 MB (28647599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d28ae42a862e9773a02317b5a0eeb71ddfe3a887bb001c8f23a2786c926287`  
		Last Modified: Thu, 16 Mar 2023 02:13:35 GMT  
		Size: 16.8 MB (16753284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6bfb39a3fef3f50b4d32c5f857a5b18f142a97de79cf264830c8ca2b9864f7`  
		Last Modified: Thu, 16 Mar 2023 02:14:17 GMT  
		Size: 43.7 MB (43738850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d39319012144c92bc4367a44b2f3e4e953b589c17b4ca366d17c8743bff813f`  
		Last Modified: Thu, 16 Mar 2023 02:14:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f074327dc8f7e760db6a5b895eb86f852bfc333785586ee10413da37f3f222`  
		Last Modified: Fri, 24 Mar 2023 20:44:10 GMT  
		Size: 278.7 MB (278679125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b051ae3be65d0725f3676e0baa40a2410ad18f0aff69131fa9715c782378cb77`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0557baee179cb29c3fd717a2a7bb1914e6f0113559f232f327cda5d986fd9a91`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd59caab82c0a6e67e3eeed26458e15e132ad27eb419aa32240ac3ac08575f5e`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 8.3 KB (8259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89595dcc22b7df58249dbec6b0679a7aa1651e536af2a463aa9d3226f9acf21d`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 1.8 MB (1774235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:9.2.0`

```console
$ docker pull solr@sha256:6a63019e5694591e2d1c53d56cdcba819235adbd1e85d91f0f82cc7562ea1ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:9.2.0` - linux; amd64

```console
$ docker pull solr@sha256:cbee52e4b6a1e30d450e8ca19402c3bc15d4d8e8a75ca8501cb0f7f642cc76ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.9 MB (374859971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d43c32e8ee6e715af99f55ba48e134125af6eadbc175932523f25a1070ce4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:44:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:46:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:46:48 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:47:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:47:22 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:07 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:52 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:20:53 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:20:54 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:20:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:20:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:21:03 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:21:03 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:21:03 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:21:03 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:21:04 GMT
USER 8983
# Fri, 24 Mar 2023 20:21:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:21:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182a611d05b01879f065473c49fb968b8d30312f931350ea07af1c46aa8b4f9`  
		Last Modified: Thu, 16 Mar 2023 02:53:08 GMT  
		Size: 17.0 MB (16975402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb51f9f63778bb9fb97f2cb054b54dfc5098aba2931664a12930c35cf464ca6`  
		Last Modified: Thu, 16 Mar 2023 02:54:00 GMT  
		Size: 46.9 MB (46935467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1365afd8cae0153f1c2bfcf8a4c9b78f2e6e0f18431b0460c63c1fede7507fee`  
		Last Modified: Thu, 16 Mar 2023 02:53:53 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b70190cd6e82c4ac613c9f0f9bf4e42155528b445617672bcd7a211b2a2104`  
		Last Modified: Fri, 24 Mar 2023 20:21:43 GMT  
		Size: 278.7 MB (278678830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c984f04f09ad32d618a63f426eb4127534ca414910aa8b56da2355a3bcf17c17`  
		Last Modified: Fri, 24 Mar 2023 20:21:31 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888b9068f218433d417da0cd83cca3863ad2cbea9bab37c09fc52a63fab6206e`  
		Last Modified: Fri, 24 Mar 2023 20:21:31 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1599d0444630b3ac11f8d61742ff79acaaec1b9cfcca5e176b131ef54c22bd`  
		Last Modified: Fri, 24 Mar 2023 20:21:32 GMT  
		Size: 8.3 KB (8264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbc52fa8b34cbd17b27c7c562e83344a928724a395e74a740d6bcfbd0aca1e8`  
		Last Modified: Fri, 24 Mar 2023 20:21:32 GMT  
		Size: 1.8 MB (1827370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.2.0` - linux; arm variant v7

```console
$ docker pull solr@sha256:7ce35f5dfe8a54b79e4886b38ee7bbae1768c5080b38dd88007711f1a730ca97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.0 MB (368994236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0c33c02e827728f7408559ce07896fbcd7ef42a58bd47bd0c340d122ef7c70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:46:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:46:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:46:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:49:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:49:36 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:50:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:50:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 21:14:57 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 21:14:57 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:15:46 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 21:15:48 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 21:15:49 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 21:15:49 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 21:15:50 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 21:15:59 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 21:16:00 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 21:16:00 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 21:16:00 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 21:16:00 GMT
USER 8983
# Fri, 24 Mar 2023 21:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 21:16:00 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:cba1fa3bcdf4f746dcf5b8f86874cee4a6eff75dd5c5cd29e4c912574b12a1c6`  
		Last Modified: Thu, 09 Mar 2023 04:41:14 GMT  
		Size: 27.0 MB (27025397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85169cff2ee4bc04fcfaf94a937435e69eb27ca38bf1dcbd04593cccacf0d702`  
		Last Modified: Thu, 16 Mar 2023 02:56:32 GMT  
		Size: 17.1 MB (17093778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be72bd479c96978965e7a3ad3512673e6ca3b26714713ca967a807e2c0bcdb7e`  
		Last Modified: Thu, 16 Mar 2023 02:57:28 GMT  
		Size: 44.5 MB (44528811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5725cdfe807b737e733d3d3a443ffd37aef0141ba7a33fb98b334c479486085`  
		Last Modified: Thu, 16 Mar 2023 02:57:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f40c0125b4d5835619a97a6e8aa526c71d7c68b45f248b530ebb09d2d1570c6`  
		Last Modified: Fri, 24 Mar 2023 21:16:36 GMT  
		Size: 278.7 MB (278680032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c884c5595959c80781c31e89baa334da69c61145587cecf73ae8777f044fbb01`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 4.2 KB (4224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387e1ea0fbb6ae2834c227fdf0661b61a1dbe74918fddc3fb294bb4dbbbce8b9`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4b5c915fbddf45760ab4310f38f8bce027f6be8d21539defc6c49238e0d1d9`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 8.3 KB (8259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c5e2d209b82002244ea91d52f9d395d4e38adde0830ca8a1a014fd6a0fb50b`  
		Last Modified: Fri, 24 Mar 2023 21:16:21 GMT  
		Size: 1.7 MB (1653357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.2.0` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:58619b9500a6637702a27985f2cf8b17cb13dae6c2673f3abaa9a1bd824277ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.6 MB (373587696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f72e1df4e02c02f553d7d54dd64951829dbdd59095775a6634ddce70eadc8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:52:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:52:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:52:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:55:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:55:04 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:55:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:55:30 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:47:31 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:47:31 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:48:14 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:48:17 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:48:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:48:17 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:48:17 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:48:18 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:48:18 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:48:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:48:27 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:48:27 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:48:27 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:48:28 GMT
USER 8983
# Fri, 24 Mar 2023 20:48:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:48:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40b70fd7935308ad0e072e7e06ec8c3abdc59beae70ca716dcd04e971680865`  
		Last Modified: Thu, 16 Mar 2023 02:00:42 GMT  
		Size: 18.4 MB (18400790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33dd5efa5ce73b25dc0236fcd408527b63e42c87e6da9672a356731004b8949`  
		Last Modified: Thu, 16 Mar 2023 02:01:25 GMT  
		Size: 46.4 MB (46421360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ce9280353ea6c4511dc5378e2f0f4742d499bf6df15c8d10804513c8c5115a`  
		Last Modified: Thu, 16 Mar 2023 02:01:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab85ed965ce21582560c60a815ae59ae9cf0fcb5c9270ba02dfc5ca1c135b44f`  
		Last Modified: Fri, 24 Mar 2023 20:49:04 GMT  
		Size: 278.7 MB (278678702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47faea25001b6a9178cab60304409e81d636878232dda7e76d519e7490bbc9`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7792e9b554723df7cdd9593ee715d8fe16cfec71a28c58e0b01e2534e7f2c8`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9435de9f76e1e09e2078c456e20cd6a83a757671ecc43398fed205b323cb3c6b`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 8.3 KB (8261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fc7a7f4116bfd1b88180e25c33fa7c4d571df7caad6ffebbec7786b32b2738`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 1.7 MB (1686320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.2.0` - linux; ppc64le

```console
$ docker pull solr@sha256:f10e0c22e5adec6e85249f7eac5f7a5f930872dbd32a9cd7c770ec7ab6077b61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.3 MB (381276492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08713b2a6558c371eb5008de184f2ae763ef7c3a322e2d740c9665f599eb2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:57:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 03:57:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 03:57:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 04:03:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:03:28 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 04:04:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 04:04:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:16:55 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:18:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:18:18 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:18:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:18:21 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:18:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:18:24 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:18:25 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:18:40 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:18:41 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:18:41 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:18:41 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:18:41 GMT
USER 8983
# Fri, 24 Mar 2023 20:18:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:18:42 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c06c33e4689e5957d961321ac18da32bea369d2eccc9173c9ad8b517f802ea`  
		Last Modified: Thu, 16 Mar 2023 04:14:09 GMT  
		Size: 18.3 MB (18257665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75be9792a67101a27b125eb6a0e465b760b4302cd2fbf3cf19338303bcfe803`  
		Last Modified: Thu, 16 Mar 2023 04:15:24 GMT  
		Size: 46.8 MB (46780948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba3f99059088b7aca45113a2e84d92786ffffd7b3920e17bc78082f1ca41023`  
		Last Modified: Thu, 16 Mar 2023 04:15:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a80e5b79ed57a03fbca62529db243f85c92ae5df2321c4e9f1224711e54a0d8`  
		Last Modified: Fri, 24 Mar 2023 20:19:29 GMT  
		Size: 278.7 MB (278679501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a83b0eea3048a8cc5ee14c0ed706cd75212e6513827c6e50ee8514b3a37ffa`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfda90d0edd877ecc2717bf59c6b25f8810ed05202ab28ba588f60de2cc3332e`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffae90319602b89f29babd93a389ad3dcb0acd2637266cdb4f1e0e4b02309a2`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 8.3 KB (8264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7a5d7ac7a4e26a6795ad596e099b124de0249d7a8cd31eff56a0786195d720`  
		Last Modified: Fri, 24 Mar 2023 20:19:07 GMT  
		Size: 1.8 MB (1833711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.2.0` - linux; s390x

```console
$ docker pull solr@sha256:55d3908647c17e61e6cc73ac71deba6d9ab2a161bd4aa7b6ea15c7a7a75fab5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369606057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1685dca8b24c2c5e320e5a7ef4c2bb2431ea293974475f5458fee07495a73e61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:06:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:06:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:06:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:07:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:07:59 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:08:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:08:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:42:43 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:43:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:43:20 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:43:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:43:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:43:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:43:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:43:27 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:43:27 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:43:27 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:43:28 GMT
USER 8983
# Fri, 24 Mar 2023 20:43:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:43:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2c7366af510b72cc0b3456fb93cfa0bfc76f7d383db5cb315967e7b1ce2e0c42`  
		Last Modified: Thu, 16 Mar 2023 02:02:40 GMT  
		Size: 28.6 MB (28647599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d28ae42a862e9773a02317b5a0eeb71ddfe3a887bb001c8f23a2786c926287`  
		Last Modified: Thu, 16 Mar 2023 02:13:35 GMT  
		Size: 16.8 MB (16753284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6bfb39a3fef3f50b4d32c5f857a5b18f142a97de79cf264830c8ca2b9864f7`  
		Last Modified: Thu, 16 Mar 2023 02:14:17 GMT  
		Size: 43.7 MB (43738850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d39319012144c92bc4367a44b2f3e4e953b589c17b4ca366d17c8743bff813f`  
		Last Modified: Thu, 16 Mar 2023 02:14:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f074327dc8f7e760db6a5b895eb86f852bfc333785586ee10413da37f3f222`  
		Last Modified: Fri, 24 Mar 2023 20:44:10 GMT  
		Size: 278.7 MB (278679125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b051ae3be65d0725f3676e0baa40a2410ad18f0aff69131fa9715c782378cb77`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0557baee179cb29c3fd717a2a7bb1914e6f0113559f232f327cda5d986fd9a91`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd59caab82c0a6e67e3eeed26458e15e132ad27eb419aa32240ac3ac08575f5e`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 8.3 KB (8259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89595dcc22b7df58249dbec6b0679a7aa1651e536af2a463aa9d3226f9acf21d`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 1.8 MB (1774235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:latest`

```console
$ docker pull solr@sha256:6a63019e5694591e2d1c53d56cdcba819235adbd1e85d91f0f82cc7562ea1ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:latest` - linux; amd64

```console
$ docker pull solr@sha256:cbee52e4b6a1e30d450e8ca19402c3bc15d4d8e8a75ca8501cb0f7f642cc76ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.9 MB (374859971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d43c32e8ee6e715af99f55ba48e134125af6eadbc175932523f25a1070ce4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:44:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:46:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:46:48 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:47:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:47:22 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:07 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:52 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:20:53 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:20:54 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:20:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:20:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:21:03 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:21:03 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:21:03 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:21:03 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:21:04 GMT
USER 8983
# Fri, 24 Mar 2023 20:21:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:21:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182a611d05b01879f065473c49fb968b8d30312f931350ea07af1c46aa8b4f9`  
		Last Modified: Thu, 16 Mar 2023 02:53:08 GMT  
		Size: 17.0 MB (16975402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb51f9f63778bb9fb97f2cb054b54dfc5098aba2931664a12930c35cf464ca6`  
		Last Modified: Thu, 16 Mar 2023 02:54:00 GMT  
		Size: 46.9 MB (46935467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1365afd8cae0153f1c2bfcf8a4c9b78f2e6e0f18431b0460c63c1fede7507fee`  
		Last Modified: Thu, 16 Mar 2023 02:53:53 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b70190cd6e82c4ac613c9f0f9bf4e42155528b445617672bcd7a211b2a2104`  
		Last Modified: Fri, 24 Mar 2023 20:21:43 GMT  
		Size: 278.7 MB (278678830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c984f04f09ad32d618a63f426eb4127534ca414910aa8b56da2355a3bcf17c17`  
		Last Modified: Fri, 24 Mar 2023 20:21:31 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888b9068f218433d417da0cd83cca3863ad2cbea9bab37c09fc52a63fab6206e`  
		Last Modified: Fri, 24 Mar 2023 20:21:31 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1599d0444630b3ac11f8d61742ff79acaaec1b9cfcca5e176b131ef54c22bd`  
		Last Modified: Fri, 24 Mar 2023 20:21:32 GMT  
		Size: 8.3 KB (8264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbc52fa8b34cbd17b27c7c562e83344a928724a395e74a740d6bcfbd0aca1e8`  
		Last Modified: Fri, 24 Mar 2023 20:21:32 GMT  
		Size: 1.8 MB (1827370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; arm variant v7

```console
$ docker pull solr@sha256:7ce35f5dfe8a54b79e4886b38ee7bbae1768c5080b38dd88007711f1a730ca97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.0 MB (368994236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0c33c02e827728f7408559ce07896fbcd7ef42a58bd47bd0c340d122ef7c70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:46:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:46:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:46:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:49:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:49:36 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:50:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:50:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 21:14:57 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 21:14:57 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:15:46 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 21:15:48 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 21:15:49 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 21:15:49 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 21:15:50 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 21:15:59 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 21:16:00 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 21:16:00 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 21:16:00 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 21:16:00 GMT
USER 8983
# Fri, 24 Mar 2023 21:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 21:16:00 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:cba1fa3bcdf4f746dcf5b8f86874cee4a6eff75dd5c5cd29e4c912574b12a1c6`  
		Last Modified: Thu, 09 Mar 2023 04:41:14 GMT  
		Size: 27.0 MB (27025397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85169cff2ee4bc04fcfaf94a937435e69eb27ca38bf1dcbd04593cccacf0d702`  
		Last Modified: Thu, 16 Mar 2023 02:56:32 GMT  
		Size: 17.1 MB (17093778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be72bd479c96978965e7a3ad3512673e6ca3b26714713ca967a807e2c0bcdb7e`  
		Last Modified: Thu, 16 Mar 2023 02:57:28 GMT  
		Size: 44.5 MB (44528811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5725cdfe807b737e733d3d3a443ffd37aef0141ba7a33fb98b334c479486085`  
		Last Modified: Thu, 16 Mar 2023 02:57:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f40c0125b4d5835619a97a6e8aa526c71d7c68b45f248b530ebb09d2d1570c6`  
		Last Modified: Fri, 24 Mar 2023 21:16:36 GMT  
		Size: 278.7 MB (278680032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c884c5595959c80781c31e89baa334da69c61145587cecf73ae8777f044fbb01`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 4.2 KB (4224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387e1ea0fbb6ae2834c227fdf0661b61a1dbe74918fddc3fb294bb4dbbbce8b9`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4b5c915fbddf45760ab4310f38f8bce027f6be8d21539defc6c49238e0d1d9`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 8.3 KB (8259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c5e2d209b82002244ea91d52f9d395d4e38adde0830ca8a1a014fd6a0fb50b`  
		Last Modified: Fri, 24 Mar 2023 21:16:21 GMT  
		Size: 1.7 MB (1653357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:58619b9500a6637702a27985f2cf8b17cb13dae6c2673f3abaa9a1bd824277ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.6 MB (373587696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f72e1df4e02c02f553d7d54dd64951829dbdd59095775a6634ddce70eadc8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:52:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:52:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:52:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:55:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:55:04 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:55:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:55:30 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:47:31 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:47:31 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:48:14 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:48:17 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:48:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:48:17 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:48:17 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:48:18 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:48:18 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:48:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:48:27 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:48:27 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:48:27 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:48:28 GMT
USER 8983
# Fri, 24 Mar 2023 20:48:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:48:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40b70fd7935308ad0e072e7e06ec8c3abdc59beae70ca716dcd04e971680865`  
		Last Modified: Thu, 16 Mar 2023 02:00:42 GMT  
		Size: 18.4 MB (18400790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33dd5efa5ce73b25dc0236fcd408527b63e42c87e6da9672a356731004b8949`  
		Last Modified: Thu, 16 Mar 2023 02:01:25 GMT  
		Size: 46.4 MB (46421360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ce9280353ea6c4511dc5378e2f0f4742d499bf6df15c8d10804513c8c5115a`  
		Last Modified: Thu, 16 Mar 2023 02:01:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab85ed965ce21582560c60a815ae59ae9cf0fcb5c9270ba02dfc5ca1c135b44f`  
		Last Modified: Fri, 24 Mar 2023 20:49:04 GMT  
		Size: 278.7 MB (278678702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47faea25001b6a9178cab60304409e81d636878232dda7e76d519e7490bbc9`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7792e9b554723df7cdd9593ee715d8fe16cfec71a28c58e0b01e2534e7f2c8`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9435de9f76e1e09e2078c456e20cd6a83a757671ecc43398fed205b323cb3c6b`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 8.3 KB (8261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fc7a7f4116bfd1b88180e25c33fa7c4d571df7caad6ffebbec7786b32b2738`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 1.7 MB (1686320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:f10e0c22e5adec6e85249f7eac5f7a5f930872dbd32a9cd7c770ec7ab6077b61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.3 MB (381276492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08713b2a6558c371eb5008de184f2ae763ef7c3a322e2d740c9665f599eb2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:57:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 03:57:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 03:57:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 04:03:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:03:28 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 04:04:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 04:04:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:16:55 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:18:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:18:18 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:18:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:18:21 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:18:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:18:24 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:18:25 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:18:40 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:18:41 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:18:41 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:18:41 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:18:41 GMT
USER 8983
# Fri, 24 Mar 2023 20:18:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:18:42 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c06c33e4689e5957d961321ac18da32bea369d2eccc9173c9ad8b517f802ea`  
		Last Modified: Thu, 16 Mar 2023 04:14:09 GMT  
		Size: 18.3 MB (18257665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75be9792a67101a27b125eb6a0e465b760b4302cd2fbf3cf19338303bcfe803`  
		Last Modified: Thu, 16 Mar 2023 04:15:24 GMT  
		Size: 46.8 MB (46780948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba3f99059088b7aca45113a2e84d92786ffffd7b3920e17bc78082f1ca41023`  
		Last Modified: Thu, 16 Mar 2023 04:15:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a80e5b79ed57a03fbca62529db243f85c92ae5df2321c4e9f1224711e54a0d8`  
		Last Modified: Fri, 24 Mar 2023 20:19:29 GMT  
		Size: 278.7 MB (278679501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a83b0eea3048a8cc5ee14c0ed706cd75212e6513827c6e50ee8514b3a37ffa`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfda90d0edd877ecc2717bf59c6b25f8810ed05202ab28ba588f60de2cc3332e`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffae90319602b89f29babd93a389ad3dcb0acd2637266cdb4f1e0e4b02309a2`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 8.3 KB (8264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7a5d7ac7a4e26a6795ad596e099b124de0249d7a8cd31eff56a0786195d720`  
		Last Modified: Fri, 24 Mar 2023 20:19:07 GMT  
		Size: 1.8 MB (1833711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:55d3908647c17e61e6cc73ac71deba6d9ab2a161bd4aa7b6ea15c7a7a75fab5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369606057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1685dca8b24c2c5e320e5a7ef4c2bb2431ea293974475f5458fee07495a73e61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:06:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:06:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:06:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:07:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:07:59 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:08:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:08:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:42:43 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:43:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:43:20 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:43:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:43:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:43:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:43:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:43:27 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:43:27 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:43:27 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:43:28 GMT
USER 8983
# Fri, 24 Mar 2023 20:43:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:43:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2c7366af510b72cc0b3456fb93cfa0bfc76f7d383db5cb315967e7b1ce2e0c42`  
		Last Modified: Thu, 16 Mar 2023 02:02:40 GMT  
		Size: 28.6 MB (28647599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d28ae42a862e9773a02317b5a0eeb71ddfe3a887bb001c8f23a2786c926287`  
		Last Modified: Thu, 16 Mar 2023 02:13:35 GMT  
		Size: 16.8 MB (16753284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6bfb39a3fef3f50b4d32c5f857a5b18f142a97de79cf264830c8ca2b9864f7`  
		Last Modified: Thu, 16 Mar 2023 02:14:17 GMT  
		Size: 43.7 MB (43738850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d39319012144c92bc4367a44b2f3e4e953b589c17b4ca366d17c8743bff813f`  
		Last Modified: Thu, 16 Mar 2023 02:14:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f074327dc8f7e760db6a5b895eb86f852bfc333785586ee10413da37f3f222`  
		Last Modified: Fri, 24 Mar 2023 20:44:10 GMT  
		Size: 278.7 MB (278679125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b051ae3be65d0725f3676e0baa40a2410ad18f0aff69131fa9715c782378cb77`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0557baee179cb29c3fd717a2a7bb1914e6f0113559f232f327cda5d986fd9a91`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd59caab82c0a6e67e3eeed26458e15e132ad27eb419aa32240ac3ac08575f5e`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 8.3 KB (8259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89595dcc22b7df58249dbec6b0679a7aa1651e536af2a463aa9d3226f9acf21d`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 1.8 MB (1774235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
