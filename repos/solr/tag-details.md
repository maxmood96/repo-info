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
-	[`solr:latest`](#solrlatest)

## `solr:8`

```console
$ docker pull solr@sha256:9519b0da29b7ebed7e66e031cf1081a2a97dbbec1fa19b06ec2e5cd4dc189210
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
$ docker pull solr@sha256:6a062c508516bf7c366eb915ebf17e339c25e90ea688f44672711c8f62f5962a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314791492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343738013924c5338d1587cd176e27563c19d81991e71105fad5ac8dc9467966`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:02:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:03:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:03:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 10:22:43 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 10:22:43 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 10:22:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 10:22:51 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 10:22:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 10:23:00 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 10:23:33 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 10:23:34 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 10:23:34 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 10:23:34 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 10:23:34 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 10:23:34 GMT
USER 8983
# Thu, 02 Mar 2023 10:23:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:23:34 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea158bec35e01412accbaee76e6548b066cd017663201fee22bf2eb3917a47b`  
		Last Modified: Thu, 02 Mar 2023 04:09:45 GMT  
		Size: 46.6 MB (46632276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48bb2059848d0df5745c7eaf26817f93c315d4cb75544b02e0354c0fa59a693`  
		Last Modified: Thu, 02 Mar 2023 04:09:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3078bc08f5e86ecde180ad8f6b8525e15be5860ecd4b6ad1f17ed9b2202ad446`  
		Last Modified: Thu, 02 Mar 2023 10:24:40 GMT  
		Size: 4.9 MB (4897328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3127728967d48f168b61cab41ce7f46e58be20a7b7de31012807e523264ddb77`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bfc8300682ebb4da32bed0f29552a1a720ca078626758378b9844b21dc9a2a`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8a8ff2af7ad5a8c98d285ddd2ee452b35d36f5b5920bab23a8f55c7e1e5658`  
		Last Modified: Thu, 02 Mar 2023 10:24:49 GMT  
		Size: 218.3 MB (218328177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a73699cb4cc82208faed9272d64625e5f8873b60fee2b3a40a3b0880fc7e7e8`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8` - linux; arm variant v7

```console
$ docker pull solr@sha256:e67e94b378772ed95b903157207c29b2bf42ca49d10e549cc6567535847325db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307139714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0def72951194fe4cf562f5890fd4f52ba987e7329e377dcf9ec724e13202a581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:45:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:45:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:47:37 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 02:48:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:48:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:45:45 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 16 Mar 2023 04:45:45 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 04:45:52 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 16 Mar 2023 04:45:52 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 16 Mar 2023 04:45:52 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 04:46:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 16 Mar 2023 04:46:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 16 Mar 2023 04:46:38 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 16 Mar 2023 04:46:38 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 04:46:38 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 04:46:38 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 04:46:38 GMT
USER 8983
# Thu, 16 Mar 2023 04:46:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 04:46:38 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a83f4fecfbc7e7f11467e3143f3a281108df95027e781d9ccaf4fa910c15f1`  
		Last Modified: Thu, 16 Mar 2023 02:53:15 GMT  
		Size: 15.2 MB (15175904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3901ceac875727d983b00901e20234573e07d14f2176888290cecbb12a175cd1`  
		Last Modified: Thu, 16 Mar 2023 02:55:26 GMT  
		Size: 44.8 MB (44843694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ed4830c84615e20b8216c2c8563b8edefbed3465745e996f2f2d8860caebf8`  
		Last Modified: Thu, 16 Mar 2023 02:55:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecea332aabc816797acc2df139f1659867d56a9a6e45b27f5f4dadc0404e4c4`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 4.2 MB (4191280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c975a37ba5769b070f8c5697351653d5e1ccfab1618dbed5ddd78676c3f493`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 4.2 KB (4221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb77cd4296384d69ce81e6dfd1666a4159f54ec5ed0364efd4054ff61792f02`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643120e9602097560d1e85d2ca1d0863873b94ad2ac19b35e3ddeb5d42a3c682`  
		Last Modified: Thu, 16 Mar 2023 04:48:22 GMT  
		Size: 218.3 MB (218328199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5389b29b6078406b5c2c4b756a5e70f7ecd60a3390ae007d305f05677d3593ac`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:aeb80771d4cfb70fa66db8496279e3b31fbd84b167a0d099f68bcb8dfb7f7adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311476661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6df42167160bb63ece3df6977769c206d43e7acd9deb7eea6f9d58d2636f570`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:51:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:52:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:53:25 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 01:54:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:54:03 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:15:55 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 16 Mar 2023 06:15:55 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 16 Mar 2023 06:15:56 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 06:15:56 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 06:16:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 16 Mar 2023 06:16:01 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 16 Mar 2023 06:16:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 06:16:10 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 16 Mar 2023 06:16:42 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 16 Mar 2023 06:16:43 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 16 Mar 2023 06:16:44 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 06:16:44 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 06:16:44 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 06:16:44 GMT
USER 8983
# Thu, 16 Mar 2023 06:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:16:44 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468a568d00c266348e3fcc790b81f74ef5577ea655a9f4ee8c5950aa335c610d`  
		Last Modified: Thu, 16 Mar 2023 01:58:03 GMT  
		Size: 16.2 MB (16210991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef260e1d5ab9e19fb72f7a2ec3268a39005c7cfe76b5fa11b8c0a1c29ad0190`  
		Last Modified: Thu, 16 Mar 2023 01:59:54 GMT  
		Size: 45.0 MB (44981027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc954dcdecda65140dfbac772a44707c39fc6e8983a24282bf19d35a583cb04`  
		Last Modified: Thu, 16 Mar 2023 01:59:49 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525ca5aa7f792125097922a398f94ed1d8a05d5343e4673c67fca19d110c3be`  
		Last Modified: Thu, 16 Mar 2023 06:17:51 GMT  
		Size: 4.7 MB (4746042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb2ed5f4ec8297d3a70b15caf26dbbad60d2bfd24e919ceb2fc0a031e38dde9`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1971ee6a5d72a5ce56c5cf73d66dc5c00ae1494a7fc266f1795214a635da7be`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 3.5 KB (3465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d60992c782c2f5643b2b30bcc2eeb237667a65e9323fc1beaf9e2c383ad98a0`  
		Last Modified: Thu, 16 Mar 2023 06:17:58 GMT  
		Size: 218.3 MB (218328174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59a3ac5ba3e4ba82a067cc5757d80bd2ba0d13825bf1b4fb2a7a395fc077ecd`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8` - linux; ppc64le

```console
$ docker pull solr@sha256:198362f62b46755605b0e864c95742bf36c4d888f6ad3a149cc4029aaab03953
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317058745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd6f4e1c4cb2c69401eb77aed21fcc57936a12d69d1771335cdd612810249b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:03:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:04:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:06:47 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:08:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:08:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 08:01:36 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 08:01:37 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 08:01:37 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 08:01:37 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 08:01:38 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 08:01:38 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 08:01:40 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 08:02:05 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 08:02:06 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 08:02:09 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 08:02:18 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 08:02:47 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 08:02:52 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 08:02:52 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 08:02:53 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 08:02:54 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 08:02:55 GMT
USER 8983
# Thu, 02 Mar 2023 08:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 08:02:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bf781428c54e99ccbf1268ef9774419ef70853536b11e51069c5ce69a81411`  
		Last Modified: Thu, 02 Mar 2023 04:17:41 GMT  
		Size: 17.6 MB (17577844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ae18692519ea6e19ae7b568af3c2b799d01a619b39daa6d2c0c6b58c9fca3`  
		Last Modified: Thu, 02 Mar 2023 04:20:36 GMT  
		Size: 42.1 MB (42063930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0838e4d8dd76f317b7f4d58ffee9c408c332049036c753c2abdce5150a06748`  
		Last Modified: Thu, 02 Mar 2023 04:20:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e441ff279834714f67bb64c7b695faa8f1960da4a3f2756d789bc36205f3c1b9`  
		Last Modified: Thu, 02 Mar 2023 08:04:42 GMT  
		Size: 5.8 MB (5774125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95ee580ffd0bac0d4d4b7d1f75fc7871f5a99ce51f7a069aee29365bfa9451e`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacd7ad985504adce4c895b47011cfc11c425432aecba2af493ffda95b12997a`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facf7fbd26499d791476a965c764fad71512ae2511e311428281371a608e41bc`  
		Last Modified: Thu, 02 Mar 2023 08:04:58 GMT  
		Size: 218.3 MB (218328234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811c7ecc40254961fbc4166e06df935d6a585b78b37ffdb467324fa3312f2b62`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 6.3 KB (6313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8` - linux; s390x

```console
$ docker pull solr@sha256:46225deee69ac78aa85f2b3d3972f1d87166c5f14a8cc48d1df86801fc572217
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306655846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3848b5e68ff932c3930fbbd9c046067ccf839eb6c254664c1fdbe7f6bce47bef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 02:26:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:26:34 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 02:27:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 02:27:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 19:33:13 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 19:33:13 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 19:33:13 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 19:33:13 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 19:33:21 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 19:33:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 19:33:23 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 19:33:30 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 19:33:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 19:34:02 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 19:34:02 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 19:34:03 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 19:34:03 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 19:34:03 GMT
USER 8983
# Thu, 02 Mar 2023 19:34:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:34:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d6ac74ab42247b9491b6986614b9868ce755dc1c84611543400690873aa73416`  
		Last Modified: Thu, 02 Mar 2023 02:22:20 GMT  
		Size: 27.0 MB (27016384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec20b82de555147dd038f63cd5be763d32cf5bd0e6a05afbaae491bfbafed5a1`  
		Last Modified: Thu, 02 Mar 2023 02:33:31 GMT  
		Size: 16.0 MB (16033099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879782d8f5dfc0f56a537f8a8ba4e15cef875216def8cdc8dde3f6e7a0e17271`  
		Last Modified: Thu, 02 Mar 2023 02:34:19 GMT  
		Size: 40.5 MB (40536858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183e8ef00bdf3c3ec288c92da3d626a4e0d27b00f537fed2b1714ac8b0e67b1`  
		Last Modified: Thu, 02 Mar 2023 02:34:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02dbc85bc5a9dd6a28499df5fe4cddbc082a0fe97e01e7b0ff65b652fe16f86`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 4.7 MB (4727022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fed773d0f1382ecb00b942174d4a5c236671c1918d8a7fe86399e858a4ff45`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0340d8812b788b38da33f58f47173802a2162d85b12af65076aca6036bdae8fb`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9dbbe7da60b5a9325818981f69392935389afdecb14a1cfcb60eecfb92c797`  
		Last Modified: Thu, 02 Mar 2023 19:35:41 GMT  
		Size: 218.3 MB (218328221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a46632aa59e9ccf2c0c6cefab6d1679d5a834f38062dae5da7e4cb035e033d`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:8-slim`

```console
$ docker pull solr@sha256:9519b0da29b7ebed7e66e031cf1081a2a97dbbec1fa19b06ec2e5cd4dc189210
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
$ docker pull solr@sha256:6a062c508516bf7c366eb915ebf17e339c25e90ea688f44672711c8f62f5962a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314791492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343738013924c5338d1587cd176e27563c19d81991e71105fad5ac8dc9467966`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:02:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:03:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:03:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 10:22:43 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 10:22:43 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 10:22:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 10:22:51 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 10:22:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 10:23:00 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 10:23:33 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 10:23:34 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 10:23:34 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 10:23:34 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 10:23:34 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 10:23:34 GMT
USER 8983
# Thu, 02 Mar 2023 10:23:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:23:34 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea158bec35e01412accbaee76e6548b066cd017663201fee22bf2eb3917a47b`  
		Last Modified: Thu, 02 Mar 2023 04:09:45 GMT  
		Size: 46.6 MB (46632276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48bb2059848d0df5745c7eaf26817f93c315d4cb75544b02e0354c0fa59a693`  
		Last Modified: Thu, 02 Mar 2023 04:09:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3078bc08f5e86ecde180ad8f6b8525e15be5860ecd4b6ad1f17ed9b2202ad446`  
		Last Modified: Thu, 02 Mar 2023 10:24:40 GMT  
		Size: 4.9 MB (4897328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3127728967d48f168b61cab41ce7f46e58be20a7b7de31012807e523264ddb77`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bfc8300682ebb4da32bed0f29552a1a720ca078626758378b9844b21dc9a2a`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8a8ff2af7ad5a8c98d285ddd2ee452b35d36f5b5920bab23a8f55c7e1e5658`  
		Last Modified: Thu, 02 Mar 2023 10:24:49 GMT  
		Size: 218.3 MB (218328177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a73699cb4cc82208faed9272d64625e5f8873b60fee2b3a40a3b0880fc7e7e8`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:e67e94b378772ed95b903157207c29b2bf42ca49d10e549cc6567535847325db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307139714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0def72951194fe4cf562f5890fd4f52ba987e7329e377dcf9ec724e13202a581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:45:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:45:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:47:37 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 02:48:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:48:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:45:45 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 16 Mar 2023 04:45:45 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 04:45:52 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 16 Mar 2023 04:45:52 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 16 Mar 2023 04:45:52 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 04:46:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 16 Mar 2023 04:46:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 16 Mar 2023 04:46:38 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 16 Mar 2023 04:46:38 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 04:46:38 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 04:46:38 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 04:46:38 GMT
USER 8983
# Thu, 16 Mar 2023 04:46:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 04:46:38 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a83f4fecfbc7e7f11467e3143f3a281108df95027e781d9ccaf4fa910c15f1`  
		Last Modified: Thu, 16 Mar 2023 02:53:15 GMT  
		Size: 15.2 MB (15175904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3901ceac875727d983b00901e20234573e07d14f2176888290cecbb12a175cd1`  
		Last Modified: Thu, 16 Mar 2023 02:55:26 GMT  
		Size: 44.8 MB (44843694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ed4830c84615e20b8216c2c8563b8edefbed3465745e996f2f2d8860caebf8`  
		Last Modified: Thu, 16 Mar 2023 02:55:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecea332aabc816797acc2df139f1659867d56a9a6e45b27f5f4dadc0404e4c4`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 4.2 MB (4191280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c975a37ba5769b070f8c5697351653d5e1ccfab1618dbed5ddd78676c3f493`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 4.2 KB (4221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb77cd4296384d69ce81e6dfd1666a4159f54ec5ed0364efd4054ff61792f02`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643120e9602097560d1e85d2ca1d0863873b94ad2ac19b35e3ddeb5d42a3c682`  
		Last Modified: Thu, 16 Mar 2023 04:48:22 GMT  
		Size: 218.3 MB (218328199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5389b29b6078406b5c2c4b756a5e70f7ecd60a3390ae007d305f05677d3593ac`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:aeb80771d4cfb70fa66db8496279e3b31fbd84b167a0d099f68bcb8dfb7f7adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311476661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6df42167160bb63ece3df6977769c206d43e7acd9deb7eea6f9d58d2636f570`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:51:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:52:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:53:25 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 01:54:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:54:03 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:15:55 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 16 Mar 2023 06:15:55 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 16 Mar 2023 06:15:56 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 06:15:56 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 06:16:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 16 Mar 2023 06:16:01 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 16 Mar 2023 06:16:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 06:16:10 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 16 Mar 2023 06:16:42 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 16 Mar 2023 06:16:43 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 16 Mar 2023 06:16:44 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 06:16:44 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 06:16:44 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 06:16:44 GMT
USER 8983
# Thu, 16 Mar 2023 06:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:16:44 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468a568d00c266348e3fcc790b81f74ef5577ea655a9f4ee8c5950aa335c610d`  
		Last Modified: Thu, 16 Mar 2023 01:58:03 GMT  
		Size: 16.2 MB (16210991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef260e1d5ab9e19fb72f7a2ec3268a39005c7cfe76b5fa11b8c0a1c29ad0190`  
		Last Modified: Thu, 16 Mar 2023 01:59:54 GMT  
		Size: 45.0 MB (44981027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc954dcdecda65140dfbac772a44707c39fc6e8983a24282bf19d35a583cb04`  
		Last Modified: Thu, 16 Mar 2023 01:59:49 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525ca5aa7f792125097922a398f94ed1d8a05d5343e4673c67fca19d110c3be`  
		Last Modified: Thu, 16 Mar 2023 06:17:51 GMT  
		Size: 4.7 MB (4746042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb2ed5f4ec8297d3a70b15caf26dbbad60d2bfd24e919ceb2fc0a031e38dde9`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1971ee6a5d72a5ce56c5cf73d66dc5c00ae1494a7fc266f1795214a635da7be`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 3.5 KB (3465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d60992c782c2f5643b2b30bcc2eeb237667a65e9323fc1beaf9e2c383ad98a0`  
		Last Modified: Thu, 16 Mar 2023 06:17:58 GMT  
		Size: 218.3 MB (218328174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59a3ac5ba3e4ba82a067cc5757d80bd2ba0d13825bf1b4fb2a7a395fc077ecd`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:198362f62b46755605b0e864c95742bf36c4d888f6ad3a149cc4029aaab03953
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317058745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd6f4e1c4cb2c69401eb77aed21fcc57936a12d69d1771335cdd612810249b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:03:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:04:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:06:47 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:08:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:08:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 08:01:36 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 08:01:37 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 08:01:37 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 08:01:37 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 08:01:38 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 08:01:38 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 08:01:40 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 08:02:05 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 08:02:06 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 08:02:09 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 08:02:18 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 08:02:47 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 08:02:52 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 08:02:52 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 08:02:53 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 08:02:54 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 08:02:55 GMT
USER 8983
# Thu, 02 Mar 2023 08:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 08:02:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bf781428c54e99ccbf1268ef9774419ef70853536b11e51069c5ce69a81411`  
		Last Modified: Thu, 02 Mar 2023 04:17:41 GMT  
		Size: 17.6 MB (17577844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ae18692519ea6e19ae7b568af3c2b799d01a619b39daa6d2c0c6b58c9fca3`  
		Last Modified: Thu, 02 Mar 2023 04:20:36 GMT  
		Size: 42.1 MB (42063930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0838e4d8dd76f317b7f4d58ffee9c408c332049036c753c2abdce5150a06748`  
		Last Modified: Thu, 02 Mar 2023 04:20:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e441ff279834714f67bb64c7b695faa8f1960da4a3f2756d789bc36205f3c1b9`  
		Last Modified: Thu, 02 Mar 2023 08:04:42 GMT  
		Size: 5.8 MB (5774125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95ee580ffd0bac0d4d4b7d1f75fc7871f5a99ce51f7a069aee29365bfa9451e`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacd7ad985504adce4c895b47011cfc11c425432aecba2af493ffda95b12997a`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facf7fbd26499d791476a965c764fad71512ae2511e311428281371a608e41bc`  
		Last Modified: Thu, 02 Mar 2023 08:04:58 GMT  
		Size: 218.3 MB (218328234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811c7ecc40254961fbc4166e06df935d6a585b78b37ffdb467324fa3312f2b62`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 6.3 KB (6313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; s390x

```console
$ docker pull solr@sha256:46225deee69ac78aa85f2b3d3972f1d87166c5f14a8cc48d1df86801fc572217
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306655846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3848b5e68ff932c3930fbbd9c046067ccf839eb6c254664c1fdbe7f6bce47bef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 02:26:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:26:34 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 02:27:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 02:27:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 19:33:13 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 19:33:13 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 19:33:13 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 19:33:13 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 19:33:21 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 19:33:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 19:33:23 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 19:33:30 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 19:33:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 19:34:02 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 19:34:02 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 19:34:03 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 19:34:03 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 19:34:03 GMT
USER 8983
# Thu, 02 Mar 2023 19:34:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:34:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d6ac74ab42247b9491b6986614b9868ce755dc1c84611543400690873aa73416`  
		Last Modified: Thu, 02 Mar 2023 02:22:20 GMT  
		Size: 27.0 MB (27016384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec20b82de555147dd038f63cd5be763d32cf5bd0e6a05afbaae491bfbafed5a1`  
		Last Modified: Thu, 02 Mar 2023 02:33:31 GMT  
		Size: 16.0 MB (16033099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879782d8f5dfc0f56a537f8a8ba4e15cef875216def8cdc8dde3f6e7a0e17271`  
		Last Modified: Thu, 02 Mar 2023 02:34:19 GMT  
		Size: 40.5 MB (40536858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183e8ef00bdf3c3ec288c92da3d626a4e0d27b00f537fed2b1714ac8b0e67b1`  
		Last Modified: Thu, 02 Mar 2023 02:34:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02dbc85bc5a9dd6a28499df5fe4cddbc082a0fe97e01e7b0ff65b652fe16f86`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 4.7 MB (4727022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fed773d0f1382ecb00b942174d4a5c236671c1918d8a7fe86399e858a4ff45`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0340d8812b788b38da33f58f47173802a2162d85b12af65076aca6036bdae8fb`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9dbbe7da60b5a9325818981f69392935389afdecb14a1cfcb60eecfb92c797`  
		Last Modified: Thu, 02 Mar 2023 19:35:41 GMT  
		Size: 218.3 MB (218328221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a46632aa59e9ccf2c0c6cefab6d1679d5a834f38062dae5da7e4cb035e033d`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:8.11`

```console
$ docker pull solr@sha256:9519b0da29b7ebed7e66e031cf1081a2a97dbbec1fa19b06ec2e5cd4dc189210
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
$ docker pull solr@sha256:6a062c508516bf7c366eb915ebf17e339c25e90ea688f44672711c8f62f5962a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314791492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343738013924c5338d1587cd176e27563c19d81991e71105fad5ac8dc9467966`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:02:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:03:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:03:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 10:22:43 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 10:22:43 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 10:22:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 10:22:51 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 10:22:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 10:23:00 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 10:23:33 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 10:23:34 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 10:23:34 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 10:23:34 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 10:23:34 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 10:23:34 GMT
USER 8983
# Thu, 02 Mar 2023 10:23:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:23:34 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea158bec35e01412accbaee76e6548b066cd017663201fee22bf2eb3917a47b`  
		Last Modified: Thu, 02 Mar 2023 04:09:45 GMT  
		Size: 46.6 MB (46632276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48bb2059848d0df5745c7eaf26817f93c315d4cb75544b02e0354c0fa59a693`  
		Last Modified: Thu, 02 Mar 2023 04:09:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3078bc08f5e86ecde180ad8f6b8525e15be5860ecd4b6ad1f17ed9b2202ad446`  
		Last Modified: Thu, 02 Mar 2023 10:24:40 GMT  
		Size: 4.9 MB (4897328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3127728967d48f168b61cab41ce7f46e58be20a7b7de31012807e523264ddb77`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bfc8300682ebb4da32bed0f29552a1a720ca078626758378b9844b21dc9a2a`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8a8ff2af7ad5a8c98d285ddd2ee452b35d36f5b5920bab23a8f55c7e1e5658`  
		Last Modified: Thu, 02 Mar 2023 10:24:49 GMT  
		Size: 218.3 MB (218328177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a73699cb4cc82208faed9272d64625e5f8873b60fee2b3a40a3b0880fc7e7e8`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11` - linux; arm variant v7

```console
$ docker pull solr@sha256:e67e94b378772ed95b903157207c29b2bf42ca49d10e549cc6567535847325db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307139714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0def72951194fe4cf562f5890fd4f52ba987e7329e377dcf9ec724e13202a581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:45:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:45:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:47:37 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 02:48:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:48:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:45:45 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 16 Mar 2023 04:45:45 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 04:45:52 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 16 Mar 2023 04:45:52 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 16 Mar 2023 04:45:52 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 04:46:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 16 Mar 2023 04:46:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 16 Mar 2023 04:46:38 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 16 Mar 2023 04:46:38 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 04:46:38 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 04:46:38 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 04:46:38 GMT
USER 8983
# Thu, 16 Mar 2023 04:46:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 04:46:38 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a83f4fecfbc7e7f11467e3143f3a281108df95027e781d9ccaf4fa910c15f1`  
		Last Modified: Thu, 16 Mar 2023 02:53:15 GMT  
		Size: 15.2 MB (15175904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3901ceac875727d983b00901e20234573e07d14f2176888290cecbb12a175cd1`  
		Last Modified: Thu, 16 Mar 2023 02:55:26 GMT  
		Size: 44.8 MB (44843694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ed4830c84615e20b8216c2c8563b8edefbed3465745e996f2f2d8860caebf8`  
		Last Modified: Thu, 16 Mar 2023 02:55:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecea332aabc816797acc2df139f1659867d56a9a6e45b27f5f4dadc0404e4c4`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 4.2 MB (4191280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c975a37ba5769b070f8c5697351653d5e1ccfab1618dbed5ddd78676c3f493`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 4.2 KB (4221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb77cd4296384d69ce81e6dfd1666a4159f54ec5ed0364efd4054ff61792f02`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643120e9602097560d1e85d2ca1d0863873b94ad2ac19b35e3ddeb5d42a3c682`  
		Last Modified: Thu, 16 Mar 2023 04:48:22 GMT  
		Size: 218.3 MB (218328199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5389b29b6078406b5c2c4b756a5e70f7ecd60a3390ae007d305f05677d3593ac`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:aeb80771d4cfb70fa66db8496279e3b31fbd84b167a0d099f68bcb8dfb7f7adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311476661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6df42167160bb63ece3df6977769c206d43e7acd9deb7eea6f9d58d2636f570`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:51:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:52:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:53:25 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 01:54:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:54:03 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:15:55 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 16 Mar 2023 06:15:55 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 16 Mar 2023 06:15:56 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 06:15:56 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 06:16:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 16 Mar 2023 06:16:01 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 16 Mar 2023 06:16:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 06:16:10 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 16 Mar 2023 06:16:42 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 16 Mar 2023 06:16:43 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 16 Mar 2023 06:16:44 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 06:16:44 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 06:16:44 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 06:16:44 GMT
USER 8983
# Thu, 16 Mar 2023 06:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:16:44 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468a568d00c266348e3fcc790b81f74ef5577ea655a9f4ee8c5950aa335c610d`  
		Last Modified: Thu, 16 Mar 2023 01:58:03 GMT  
		Size: 16.2 MB (16210991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef260e1d5ab9e19fb72f7a2ec3268a39005c7cfe76b5fa11b8c0a1c29ad0190`  
		Last Modified: Thu, 16 Mar 2023 01:59:54 GMT  
		Size: 45.0 MB (44981027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc954dcdecda65140dfbac772a44707c39fc6e8983a24282bf19d35a583cb04`  
		Last Modified: Thu, 16 Mar 2023 01:59:49 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525ca5aa7f792125097922a398f94ed1d8a05d5343e4673c67fca19d110c3be`  
		Last Modified: Thu, 16 Mar 2023 06:17:51 GMT  
		Size: 4.7 MB (4746042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb2ed5f4ec8297d3a70b15caf26dbbad60d2bfd24e919ceb2fc0a031e38dde9`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1971ee6a5d72a5ce56c5cf73d66dc5c00ae1494a7fc266f1795214a635da7be`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 3.5 KB (3465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d60992c782c2f5643b2b30bcc2eeb237667a65e9323fc1beaf9e2c383ad98a0`  
		Last Modified: Thu, 16 Mar 2023 06:17:58 GMT  
		Size: 218.3 MB (218328174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59a3ac5ba3e4ba82a067cc5757d80bd2ba0d13825bf1b4fb2a7a395fc077ecd`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11` - linux; ppc64le

```console
$ docker pull solr@sha256:198362f62b46755605b0e864c95742bf36c4d888f6ad3a149cc4029aaab03953
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317058745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd6f4e1c4cb2c69401eb77aed21fcc57936a12d69d1771335cdd612810249b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:03:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:04:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:06:47 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:08:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:08:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 08:01:36 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 08:01:37 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 08:01:37 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 08:01:37 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 08:01:38 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 08:01:38 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 08:01:40 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 08:02:05 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 08:02:06 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 08:02:09 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 08:02:18 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 08:02:47 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 08:02:52 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 08:02:52 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 08:02:53 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 08:02:54 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 08:02:55 GMT
USER 8983
# Thu, 02 Mar 2023 08:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 08:02:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bf781428c54e99ccbf1268ef9774419ef70853536b11e51069c5ce69a81411`  
		Last Modified: Thu, 02 Mar 2023 04:17:41 GMT  
		Size: 17.6 MB (17577844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ae18692519ea6e19ae7b568af3c2b799d01a619b39daa6d2c0c6b58c9fca3`  
		Last Modified: Thu, 02 Mar 2023 04:20:36 GMT  
		Size: 42.1 MB (42063930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0838e4d8dd76f317b7f4d58ffee9c408c332049036c753c2abdce5150a06748`  
		Last Modified: Thu, 02 Mar 2023 04:20:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e441ff279834714f67bb64c7b695faa8f1960da4a3f2756d789bc36205f3c1b9`  
		Last Modified: Thu, 02 Mar 2023 08:04:42 GMT  
		Size: 5.8 MB (5774125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95ee580ffd0bac0d4d4b7d1f75fc7871f5a99ce51f7a069aee29365bfa9451e`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacd7ad985504adce4c895b47011cfc11c425432aecba2af493ffda95b12997a`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facf7fbd26499d791476a965c764fad71512ae2511e311428281371a608e41bc`  
		Last Modified: Thu, 02 Mar 2023 08:04:58 GMT  
		Size: 218.3 MB (218328234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811c7ecc40254961fbc4166e06df935d6a585b78b37ffdb467324fa3312f2b62`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 6.3 KB (6313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11` - linux; s390x

```console
$ docker pull solr@sha256:46225deee69ac78aa85f2b3d3972f1d87166c5f14a8cc48d1df86801fc572217
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306655846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3848b5e68ff932c3930fbbd9c046067ccf839eb6c254664c1fdbe7f6bce47bef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 02:26:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:26:34 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 02:27:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 02:27:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 19:33:13 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 19:33:13 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 19:33:13 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 19:33:13 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 19:33:21 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 19:33:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 19:33:23 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 19:33:30 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 19:33:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 19:34:02 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 19:34:02 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 19:34:03 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 19:34:03 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 19:34:03 GMT
USER 8983
# Thu, 02 Mar 2023 19:34:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:34:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d6ac74ab42247b9491b6986614b9868ce755dc1c84611543400690873aa73416`  
		Last Modified: Thu, 02 Mar 2023 02:22:20 GMT  
		Size: 27.0 MB (27016384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec20b82de555147dd038f63cd5be763d32cf5bd0e6a05afbaae491bfbafed5a1`  
		Last Modified: Thu, 02 Mar 2023 02:33:31 GMT  
		Size: 16.0 MB (16033099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879782d8f5dfc0f56a537f8a8ba4e15cef875216def8cdc8dde3f6e7a0e17271`  
		Last Modified: Thu, 02 Mar 2023 02:34:19 GMT  
		Size: 40.5 MB (40536858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183e8ef00bdf3c3ec288c92da3d626a4e0d27b00f537fed2b1714ac8b0e67b1`  
		Last Modified: Thu, 02 Mar 2023 02:34:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02dbc85bc5a9dd6a28499df5fe4cddbc082a0fe97e01e7b0ff65b652fe16f86`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 4.7 MB (4727022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fed773d0f1382ecb00b942174d4a5c236671c1918d8a7fe86399e858a4ff45`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0340d8812b788b38da33f58f47173802a2162d85b12af65076aca6036bdae8fb`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9dbbe7da60b5a9325818981f69392935389afdecb14a1cfcb60eecfb92c797`  
		Last Modified: Thu, 02 Mar 2023 19:35:41 GMT  
		Size: 218.3 MB (218328221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a46632aa59e9ccf2c0c6cefab6d1679d5a834f38062dae5da7e4cb035e033d`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:8.11-slim`

```console
$ docker pull solr@sha256:9519b0da29b7ebed7e66e031cf1081a2a97dbbec1fa19b06ec2e5cd4dc189210
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
$ docker pull solr@sha256:6a062c508516bf7c366eb915ebf17e339c25e90ea688f44672711c8f62f5962a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314791492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343738013924c5338d1587cd176e27563c19d81991e71105fad5ac8dc9467966`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:02:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:03:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:03:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 10:22:43 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 10:22:43 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 10:22:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 10:22:51 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 10:22:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 10:23:00 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 10:23:33 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 10:23:34 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 10:23:34 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 10:23:34 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 10:23:34 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 10:23:34 GMT
USER 8983
# Thu, 02 Mar 2023 10:23:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:23:34 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea158bec35e01412accbaee76e6548b066cd017663201fee22bf2eb3917a47b`  
		Last Modified: Thu, 02 Mar 2023 04:09:45 GMT  
		Size: 46.6 MB (46632276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48bb2059848d0df5745c7eaf26817f93c315d4cb75544b02e0354c0fa59a693`  
		Last Modified: Thu, 02 Mar 2023 04:09:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3078bc08f5e86ecde180ad8f6b8525e15be5860ecd4b6ad1f17ed9b2202ad446`  
		Last Modified: Thu, 02 Mar 2023 10:24:40 GMT  
		Size: 4.9 MB (4897328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3127728967d48f168b61cab41ce7f46e58be20a7b7de31012807e523264ddb77`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bfc8300682ebb4da32bed0f29552a1a720ca078626758378b9844b21dc9a2a`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8a8ff2af7ad5a8c98d285ddd2ee452b35d36f5b5920bab23a8f55c7e1e5658`  
		Last Modified: Thu, 02 Mar 2023 10:24:49 GMT  
		Size: 218.3 MB (218328177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a73699cb4cc82208faed9272d64625e5f8873b60fee2b3a40a3b0880fc7e7e8`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11-slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:e67e94b378772ed95b903157207c29b2bf42ca49d10e549cc6567535847325db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307139714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0def72951194fe4cf562f5890fd4f52ba987e7329e377dcf9ec724e13202a581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:45:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:45:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:47:37 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 02:48:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:48:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:45:45 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 16 Mar 2023 04:45:45 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 04:45:52 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 16 Mar 2023 04:45:52 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 16 Mar 2023 04:45:52 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 04:46:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 16 Mar 2023 04:46:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 16 Mar 2023 04:46:38 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 16 Mar 2023 04:46:38 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 04:46:38 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 04:46:38 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 04:46:38 GMT
USER 8983
# Thu, 16 Mar 2023 04:46:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 04:46:38 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a83f4fecfbc7e7f11467e3143f3a281108df95027e781d9ccaf4fa910c15f1`  
		Last Modified: Thu, 16 Mar 2023 02:53:15 GMT  
		Size: 15.2 MB (15175904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3901ceac875727d983b00901e20234573e07d14f2176888290cecbb12a175cd1`  
		Last Modified: Thu, 16 Mar 2023 02:55:26 GMT  
		Size: 44.8 MB (44843694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ed4830c84615e20b8216c2c8563b8edefbed3465745e996f2f2d8860caebf8`  
		Last Modified: Thu, 16 Mar 2023 02:55:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecea332aabc816797acc2df139f1659867d56a9a6e45b27f5f4dadc0404e4c4`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 4.2 MB (4191280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c975a37ba5769b070f8c5697351653d5e1ccfab1618dbed5ddd78676c3f493`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 4.2 KB (4221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb77cd4296384d69ce81e6dfd1666a4159f54ec5ed0364efd4054ff61792f02`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643120e9602097560d1e85d2ca1d0863873b94ad2ac19b35e3ddeb5d42a3c682`  
		Last Modified: Thu, 16 Mar 2023 04:48:22 GMT  
		Size: 218.3 MB (218328199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5389b29b6078406b5c2c4b756a5e70f7ecd60a3390ae007d305f05677d3593ac`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:aeb80771d4cfb70fa66db8496279e3b31fbd84b167a0d099f68bcb8dfb7f7adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311476661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6df42167160bb63ece3df6977769c206d43e7acd9deb7eea6f9d58d2636f570`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:51:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:52:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:53:25 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 01:54:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:54:03 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:15:55 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 16 Mar 2023 06:15:55 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 16 Mar 2023 06:15:56 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 06:15:56 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 06:16:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 16 Mar 2023 06:16:01 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 16 Mar 2023 06:16:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 06:16:10 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 16 Mar 2023 06:16:42 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 16 Mar 2023 06:16:43 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 16 Mar 2023 06:16:44 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 06:16:44 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 06:16:44 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 06:16:44 GMT
USER 8983
# Thu, 16 Mar 2023 06:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:16:44 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468a568d00c266348e3fcc790b81f74ef5577ea655a9f4ee8c5950aa335c610d`  
		Last Modified: Thu, 16 Mar 2023 01:58:03 GMT  
		Size: 16.2 MB (16210991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef260e1d5ab9e19fb72f7a2ec3268a39005c7cfe76b5fa11b8c0a1c29ad0190`  
		Last Modified: Thu, 16 Mar 2023 01:59:54 GMT  
		Size: 45.0 MB (44981027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc954dcdecda65140dfbac772a44707c39fc6e8983a24282bf19d35a583cb04`  
		Last Modified: Thu, 16 Mar 2023 01:59:49 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525ca5aa7f792125097922a398f94ed1d8a05d5343e4673c67fca19d110c3be`  
		Last Modified: Thu, 16 Mar 2023 06:17:51 GMT  
		Size: 4.7 MB (4746042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb2ed5f4ec8297d3a70b15caf26dbbad60d2bfd24e919ceb2fc0a031e38dde9`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1971ee6a5d72a5ce56c5cf73d66dc5c00ae1494a7fc266f1795214a635da7be`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 3.5 KB (3465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d60992c782c2f5643b2b30bcc2eeb237667a65e9323fc1beaf9e2c383ad98a0`  
		Last Modified: Thu, 16 Mar 2023 06:17:58 GMT  
		Size: 218.3 MB (218328174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59a3ac5ba3e4ba82a067cc5757d80bd2ba0d13825bf1b4fb2a7a395fc077ecd`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:198362f62b46755605b0e864c95742bf36c4d888f6ad3a149cc4029aaab03953
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317058745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd6f4e1c4cb2c69401eb77aed21fcc57936a12d69d1771335cdd612810249b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:03:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:04:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:06:47 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:08:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:08:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 08:01:36 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 08:01:37 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 08:01:37 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 08:01:37 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 08:01:38 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 08:01:38 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 08:01:40 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 08:02:05 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 08:02:06 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 08:02:09 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 08:02:18 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 08:02:47 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 08:02:52 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 08:02:52 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 08:02:53 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 08:02:54 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 08:02:55 GMT
USER 8983
# Thu, 02 Mar 2023 08:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 08:02:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bf781428c54e99ccbf1268ef9774419ef70853536b11e51069c5ce69a81411`  
		Last Modified: Thu, 02 Mar 2023 04:17:41 GMT  
		Size: 17.6 MB (17577844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ae18692519ea6e19ae7b568af3c2b799d01a619b39daa6d2c0c6b58c9fca3`  
		Last Modified: Thu, 02 Mar 2023 04:20:36 GMT  
		Size: 42.1 MB (42063930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0838e4d8dd76f317b7f4d58ffee9c408c332049036c753c2abdce5150a06748`  
		Last Modified: Thu, 02 Mar 2023 04:20:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e441ff279834714f67bb64c7b695faa8f1960da4a3f2756d789bc36205f3c1b9`  
		Last Modified: Thu, 02 Mar 2023 08:04:42 GMT  
		Size: 5.8 MB (5774125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95ee580ffd0bac0d4d4b7d1f75fc7871f5a99ce51f7a069aee29365bfa9451e`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacd7ad985504adce4c895b47011cfc11c425432aecba2af493ffda95b12997a`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facf7fbd26499d791476a965c764fad71512ae2511e311428281371a608e41bc`  
		Last Modified: Thu, 02 Mar 2023 08:04:58 GMT  
		Size: 218.3 MB (218328234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811c7ecc40254961fbc4166e06df935d6a585b78b37ffdb467324fa3312f2b62`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 6.3 KB (6313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11-slim` - linux; s390x

```console
$ docker pull solr@sha256:46225deee69ac78aa85f2b3d3972f1d87166c5f14a8cc48d1df86801fc572217
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306655846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3848b5e68ff932c3930fbbd9c046067ccf839eb6c254664c1fdbe7f6bce47bef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 02:26:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:26:34 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 02:27:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 02:27:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 19:33:13 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 19:33:13 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 19:33:13 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 19:33:13 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 19:33:21 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 19:33:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 19:33:23 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 19:33:30 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 19:33:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 19:34:02 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 19:34:02 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 19:34:03 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 19:34:03 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 19:34:03 GMT
USER 8983
# Thu, 02 Mar 2023 19:34:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:34:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d6ac74ab42247b9491b6986614b9868ce755dc1c84611543400690873aa73416`  
		Last Modified: Thu, 02 Mar 2023 02:22:20 GMT  
		Size: 27.0 MB (27016384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec20b82de555147dd038f63cd5be763d32cf5bd0e6a05afbaae491bfbafed5a1`  
		Last Modified: Thu, 02 Mar 2023 02:33:31 GMT  
		Size: 16.0 MB (16033099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879782d8f5dfc0f56a537f8a8ba4e15cef875216def8cdc8dde3f6e7a0e17271`  
		Last Modified: Thu, 02 Mar 2023 02:34:19 GMT  
		Size: 40.5 MB (40536858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183e8ef00bdf3c3ec288c92da3d626a4e0d27b00f537fed2b1714ac8b0e67b1`  
		Last Modified: Thu, 02 Mar 2023 02:34:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02dbc85bc5a9dd6a28499df5fe4cddbc082a0fe97e01e7b0ff65b652fe16f86`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 4.7 MB (4727022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fed773d0f1382ecb00b942174d4a5c236671c1918d8a7fe86399e858a4ff45`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0340d8812b788b38da33f58f47173802a2162d85b12af65076aca6036bdae8fb`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9dbbe7da60b5a9325818981f69392935389afdecb14a1cfcb60eecfb92c797`  
		Last Modified: Thu, 02 Mar 2023 19:35:41 GMT  
		Size: 218.3 MB (218328221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a46632aa59e9ccf2c0c6cefab6d1679d5a834f38062dae5da7e4cb035e033d`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:8.11.2`

```console
$ docker pull solr@sha256:9519b0da29b7ebed7e66e031cf1081a2a97dbbec1fa19b06ec2e5cd4dc189210
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
$ docker pull solr@sha256:6a062c508516bf7c366eb915ebf17e339c25e90ea688f44672711c8f62f5962a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314791492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343738013924c5338d1587cd176e27563c19d81991e71105fad5ac8dc9467966`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:02:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:03:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:03:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 10:22:43 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 10:22:43 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 10:22:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 10:22:51 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 10:22:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 10:23:00 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 10:23:33 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 10:23:34 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 10:23:34 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 10:23:34 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 10:23:34 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 10:23:34 GMT
USER 8983
# Thu, 02 Mar 2023 10:23:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:23:34 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea158bec35e01412accbaee76e6548b066cd017663201fee22bf2eb3917a47b`  
		Last Modified: Thu, 02 Mar 2023 04:09:45 GMT  
		Size: 46.6 MB (46632276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48bb2059848d0df5745c7eaf26817f93c315d4cb75544b02e0354c0fa59a693`  
		Last Modified: Thu, 02 Mar 2023 04:09:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3078bc08f5e86ecde180ad8f6b8525e15be5860ecd4b6ad1f17ed9b2202ad446`  
		Last Modified: Thu, 02 Mar 2023 10:24:40 GMT  
		Size: 4.9 MB (4897328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3127728967d48f168b61cab41ce7f46e58be20a7b7de31012807e523264ddb77`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bfc8300682ebb4da32bed0f29552a1a720ca078626758378b9844b21dc9a2a`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8a8ff2af7ad5a8c98d285ddd2ee452b35d36f5b5920bab23a8f55c7e1e5658`  
		Last Modified: Thu, 02 Mar 2023 10:24:49 GMT  
		Size: 218.3 MB (218328177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a73699cb4cc82208faed9272d64625e5f8873b60fee2b3a40a3b0880fc7e7e8`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2` - linux; arm variant v7

```console
$ docker pull solr@sha256:e67e94b378772ed95b903157207c29b2bf42ca49d10e549cc6567535847325db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307139714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0def72951194fe4cf562f5890fd4f52ba987e7329e377dcf9ec724e13202a581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:45:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:45:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:47:37 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 02:48:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:48:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:45:45 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 16 Mar 2023 04:45:45 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 04:45:52 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 16 Mar 2023 04:45:52 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 16 Mar 2023 04:45:52 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 04:46:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 16 Mar 2023 04:46:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 16 Mar 2023 04:46:38 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 16 Mar 2023 04:46:38 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 04:46:38 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 04:46:38 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 04:46:38 GMT
USER 8983
# Thu, 16 Mar 2023 04:46:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 04:46:38 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a83f4fecfbc7e7f11467e3143f3a281108df95027e781d9ccaf4fa910c15f1`  
		Last Modified: Thu, 16 Mar 2023 02:53:15 GMT  
		Size: 15.2 MB (15175904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3901ceac875727d983b00901e20234573e07d14f2176888290cecbb12a175cd1`  
		Last Modified: Thu, 16 Mar 2023 02:55:26 GMT  
		Size: 44.8 MB (44843694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ed4830c84615e20b8216c2c8563b8edefbed3465745e996f2f2d8860caebf8`  
		Last Modified: Thu, 16 Mar 2023 02:55:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecea332aabc816797acc2df139f1659867d56a9a6e45b27f5f4dadc0404e4c4`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 4.2 MB (4191280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c975a37ba5769b070f8c5697351653d5e1ccfab1618dbed5ddd78676c3f493`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 4.2 KB (4221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb77cd4296384d69ce81e6dfd1666a4159f54ec5ed0364efd4054ff61792f02`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643120e9602097560d1e85d2ca1d0863873b94ad2ac19b35e3ddeb5d42a3c682`  
		Last Modified: Thu, 16 Mar 2023 04:48:22 GMT  
		Size: 218.3 MB (218328199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5389b29b6078406b5c2c4b756a5e70f7ecd60a3390ae007d305f05677d3593ac`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:aeb80771d4cfb70fa66db8496279e3b31fbd84b167a0d099f68bcb8dfb7f7adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311476661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6df42167160bb63ece3df6977769c206d43e7acd9deb7eea6f9d58d2636f570`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:51:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:52:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:53:25 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 01:54:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:54:03 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:15:55 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 16 Mar 2023 06:15:55 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 16 Mar 2023 06:15:56 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 06:15:56 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 06:16:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 16 Mar 2023 06:16:01 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 16 Mar 2023 06:16:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 06:16:10 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 16 Mar 2023 06:16:42 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 16 Mar 2023 06:16:43 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 16 Mar 2023 06:16:44 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 06:16:44 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 06:16:44 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 06:16:44 GMT
USER 8983
# Thu, 16 Mar 2023 06:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:16:44 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468a568d00c266348e3fcc790b81f74ef5577ea655a9f4ee8c5950aa335c610d`  
		Last Modified: Thu, 16 Mar 2023 01:58:03 GMT  
		Size: 16.2 MB (16210991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef260e1d5ab9e19fb72f7a2ec3268a39005c7cfe76b5fa11b8c0a1c29ad0190`  
		Last Modified: Thu, 16 Mar 2023 01:59:54 GMT  
		Size: 45.0 MB (44981027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc954dcdecda65140dfbac772a44707c39fc6e8983a24282bf19d35a583cb04`  
		Last Modified: Thu, 16 Mar 2023 01:59:49 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525ca5aa7f792125097922a398f94ed1d8a05d5343e4673c67fca19d110c3be`  
		Last Modified: Thu, 16 Mar 2023 06:17:51 GMT  
		Size: 4.7 MB (4746042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb2ed5f4ec8297d3a70b15caf26dbbad60d2bfd24e919ceb2fc0a031e38dde9`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1971ee6a5d72a5ce56c5cf73d66dc5c00ae1494a7fc266f1795214a635da7be`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 3.5 KB (3465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d60992c782c2f5643b2b30bcc2eeb237667a65e9323fc1beaf9e2c383ad98a0`  
		Last Modified: Thu, 16 Mar 2023 06:17:58 GMT  
		Size: 218.3 MB (218328174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59a3ac5ba3e4ba82a067cc5757d80bd2ba0d13825bf1b4fb2a7a395fc077ecd`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2` - linux; ppc64le

```console
$ docker pull solr@sha256:198362f62b46755605b0e864c95742bf36c4d888f6ad3a149cc4029aaab03953
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317058745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd6f4e1c4cb2c69401eb77aed21fcc57936a12d69d1771335cdd612810249b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:03:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:04:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:06:47 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:08:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:08:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 08:01:36 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 08:01:37 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 08:01:37 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 08:01:37 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 08:01:38 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 08:01:38 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 08:01:40 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 08:02:05 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 08:02:06 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 08:02:09 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 08:02:18 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 08:02:47 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 08:02:52 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 08:02:52 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 08:02:53 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 08:02:54 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 08:02:55 GMT
USER 8983
# Thu, 02 Mar 2023 08:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 08:02:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bf781428c54e99ccbf1268ef9774419ef70853536b11e51069c5ce69a81411`  
		Last Modified: Thu, 02 Mar 2023 04:17:41 GMT  
		Size: 17.6 MB (17577844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ae18692519ea6e19ae7b568af3c2b799d01a619b39daa6d2c0c6b58c9fca3`  
		Last Modified: Thu, 02 Mar 2023 04:20:36 GMT  
		Size: 42.1 MB (42063930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0838e4d8dd76f317b7f4d58ffee9c408c332049036c753c2abdce5150a06748`  
		Last Modified: Thu, 02 Mar 2023 04:20:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e441ff279834714f67bb64c7b695faa8f1960da4a3f2756d789bc36205f3c1b9`  
		Last Modified: Thu, 02 Mar 2023 08:04:42 GMT  
		Size: 5.8 MB (5774125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95ee580ffd0bac0d4d4b7d1f75fc7871f5a99ce51f7a069aee29365bfa9451e`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacd7ad985504adce4c895b47011cfc11c425432aecba2af493ffda95b12997a`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facf7fbd26499d791476a965c764fad71512ae2511e311428281371a608e41bc`  
		Last Modified: Thu, 02 Mar 2023 08:04:58 GMT  
		Size: 218.3 MB (218328234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811c7ecc40254961fbc4166e06df935d6a585b78b37ffdb467324fa3312f2b62`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 6.3 KB (6313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2` - linux; s390x

```console
$ docker pull solr@sha256:46225deee69ac78aa85f2b3d3972f1d87166c5f14a8cc48d1df86801fc572217
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306655846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3848b5e68ff932c3930fbbd9c046067ccf839eb6c254664c1fdbe7f6bce47bef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 02:26:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:26:34 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 02:27:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 02:27:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 19:33:13 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 19:33:13 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 19:33:13 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 19:33:13 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 19:33:21 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 19:33:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 19:33:23 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 19:33:30 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 19:33:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 19:34:02 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 19:34:02 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 19:34:03 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 19:34:03 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 19:34:03 GMT
USER 8983
# Thu, 02 Mar 2023 19:34:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:34:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d6ac74ab42247b9491b6986614b9868ce755dc1c84611543400690873aa73416`  
		Last Modified: Thu, 02 Mar 2023 02:22:20 GMT  
		Size: 27.0 MB (27016384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec20b82de555147dd038f63cd5be763d32cf5bd0e6a05afbaae491bfbafed5a1`  
		Last Modified: Thu, 02 Mar 2023 02:33:31 GMT  
		Size: 16.0 MB (16033099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879782d8f5dfc0f56a537f8a8ba4e15cef875216def8cdc8dde3f6e7a0e17271`  
		Last Modified: Thu, 02 Mar 2023 02:34:19 GMT  
		Size: 40.5 MB (40536858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183e8ef00bdf3c3ec288c92da3d626a4e0d27b00f537fed2b1714ac8b0e67b1`  
		Last Modified: Thu, 02 Mar 2023 02:34:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02dbc85bc5a9dd6a28499df5fe4cddbc082a0fe97e01e7b0ff65b652fe16f86`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 4.7 MB (4727022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fed773d0f1382ecb00b942174d4a5c236671c1918d8a7fe86399e858a4ff45`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0340d8812b788b38da33f58f47173802a2162d85b12af65076aca6036bdae8fb`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9dbbe7da60b5a9325818981f69392935389afdecb14a1cfcb60eecfb92c797`  
		Last Modified: Thu, 02 Mar 2023 19:35:41 GMT  
		Size: 218.3 MB (218328221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a46632aa59e9ccf2c0c6cefab6d1679d5a834f38062dae5da7e4cb035e033d`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:8.11.2-slim`

```console
$ docker pull solr@sha256:9519b0da29b7ebed7e66e031cf1081a2a97dbbec1fa19b06ec2e5cd4dc189210
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
$ docker pull solr@sha256:6a062c508516bf7c366eb915ebf17e339c25e90ea688f44672711c8f62f5962a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314791492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343738013924c5338d1587cd176e27563c19d81991e71105fad5ac8dc9467966`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:01:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:02:28 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:03:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:03:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 10:22:43 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 10:22:43 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 10:22:43 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 10:22:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 10:22:51 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 10:22:51 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 10:23:00 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 10:23:33 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 10:23:34 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 10:23:34 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 10:23:34 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 10:23:34 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 10:23:34 GMT
USER 8983
# Thu, 02 Mar 2023 10:23:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:23:34 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7015360bd1b0c50709c39c29445410d9103f250a78c1f0067f535569434606e`  
		Last Modified: Thu, 02 Mar 2023 04:07:42 GMT  
		Size: 16.3 MB (16341483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea158bec35e01412accbaee76e6548b066cd017663201fee22bf2eb3917a47b`  
		Last Modified: Thu, 02 Mar 2023 04:09:45 GMT  
		Size: 46.6 MB (46632276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48bb2059848d0df5745c7eaf26817f93c315d4cb75544b02e0354c0fa59a693`  
		Last Modified: Thu, 02 Mar 2023 04:09:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3078bc08f5e86ecde180ad8f6b8525e15be5860ecd4b6ad1f17ed9b2202ad446`  
		Last Modified: Thu, 02 Mar 2023 10:24:40 GMT  
		Size: 4.9 MB (4897328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3127728967d48f168b61cab41ce7f46e58be20a7b7de31012807e523264ddb77`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bfc8300682ebb4da32bed0f29552a1a720ca078626758378b9844b21dc9a2a`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8a8ff2af7ad5a8c98d285ddd2ee452b35d36f5b5920bab23a8f55c7e1e5658`  
		Last Modified: Thu, 02 Mar 2023 10:24:49 GMT  
		Size: 218.3 MB (218328177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a73699cb4cc82208faed9272d64625e5f8873b60fee2b3a40a3b0880fc7e7e8`  
		Last Modified: Thu, 02 Mar 2023 10:24:39 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2-slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:e67e94b378772ed95b903157207c29b2bf42ca49d10e549cc6567535847325db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307139714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0def72951194fe4cf562f5890fd4f52ba987e7329e377dcf9ec724e13202a581`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:45:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:45:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:47:37 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 02:48:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:48:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:45:45 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 16 Mar 2023 04:45:45 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 04:45:46 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 04:45:52 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 16 Mar 2023 04:45:52 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 16 Mar 2023 04:45:52 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 04:46:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 16 Mar 2023 04:46:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 16 Mar 2023 04:46:38 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 16 Mar 2023 04:46:38 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 04:46:38 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 04:46:38 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 04:46:38 GMT
USER 8983
# Thu, 16 Mar 2023 04:46:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 04:46:38 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a83f4fecfbc7e7f11467e3143f3a281108df95027e781d9ccaf4fa910c15f1`  
		Last Modified: Thu, 16 Mar 2023 02:53:15 GMT  
		Size: 15.2 MB (15175904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3901ceac875727d983b00901e20234573e07d14f2176888290cecbb12a175cd1`  
		Last Modified: Thu, 16 Mar 2023 02:55:26 GMT  
		Size: 44.8 MB (44843694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ed4830c84615e20b8216c2c8563b8edefbed3465745e996f2f2d8860caebf8`  
		Last Modified: Thu, 16 Mar 2023 02:55:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecea332aabc816797acc2df139f1659867d56a9a6e45b27f5f4dadc0404e4c4`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 4.2 MB (4191280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c975a37ba5769b070f8c5697351653d5e1ccfab1618dbed5ddd78676c3f493`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 4.2 KB (4221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb77cd4296384d69ce81e6dfd1666a4159f54ec5ed0364efd4054ff61792f02`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 3.5 KB (3467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643120e9602097560d1e85d2ca1d0863873b94ad2ac19b35e3ddeb5d42a3c682`  
		Last Modified: Thu, 16 Mar 2023 04:48:22 GMT  
		Size: 218.3 MB (218328199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5389b29b6078406b5c2c4b756a5e70f7ecd60a3390ae007d305f05677d3593ac`  
		Last Modified: Thu, 16 Mar 2023 04:48:11 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:aeb80771d4cfb70fa66db8496279e3b31fbd84b167a0d099f68bcb8dfb7f7adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311476661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6df42167160bb63ece3df6977769c206d43e7acd9deb7eea6f9d58d2636f570`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:51:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:52:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:53:25 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 16 Mar 2023 01:54:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:54:03 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:15:55 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 16 Mar 2023 06:15:55 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 16 Mar 2023 06:15:55 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 16 Mar 2023 06:15:56 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 06:15:56 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 06:16:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 16 Mar 2023 06:16:01 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 16 Mar 2023 06:16:01 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 06:16:10 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 16 Mar 2023 06:16:42 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 16 Mar 2023 06:16:43 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 16 Mar 2023 06:16:44 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 06:16:44 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 06:16:44 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 06:16:44 GMT
USER 8983
# Thu, 16 Mar 2023 06:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:16:44 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468a568d00c266348e3fcc790b81f74ef5577ea655a9f4ee8c5950aa335c610d`  
		Last Modified: Thu, 16 Mar 2023 01:58:03 GMT  
		Size: 16.2 MB (16210991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef260e1d5ab9e19fb72f7a2ec3268a39005c7cfe76b5fa11b8c0a1c29ad0190`  
		Last Modified: Thu, 16 Mar 2023 01:59:54 GMT  
		Size: 45.0 MB (44981027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc954dcdecda65140dfbac772a44707c39fc6e8983a24282bf19d35a583cb04`  
		Last Modified: Thu, 16 Mar 2023 01:59:49 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9525ca5aa7f792125097922a398f94ed1d8a05d5343e4673c67fca19d110c3be`  
		Last Modified: Thu, 16 Mar 2023 06:17:51 GMT  
		Size: 4.7 MB (4746042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb2ed5f4ec8297d3a70b15caf26dbbad60d2bfd24e919ceb2fc0a031e38dde9`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1971ee6a5d72a5ce56c5cf73d66dc5c00ae1494a7fc266f1795214a635da7be`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 3.5 KB (3465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d60992c782c2f5643b2b30bcc2eeb237667a65e9323fc1beaf9e2c383ad98a0`  
		Last Modified: Thu, 16 Mar 2023 06:17:58 GMT  
		Size: 218.3 MB (218328174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59a3ac5ba3e4ba82a067cc5757d80bd2ba0d13825bf1b4fb2a7a395fc077ecd`  
		Last Modified: Thu, 16 Mar 2023 06:17:50 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:198362f62b46755605b0e864c95742bf36c4d888f6ad3a149cc4029aaab03953
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317058745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd6f4e1c4cb2c69401eb77aed21fcc57936a12d69d1771335cdd612810249b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:03:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:04:14 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:06:47 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 04:08:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:08:18 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 08:01:36 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 08:01:37 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 08:01:37 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 08:01:37 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 08:01:38 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 08:01:38 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 08:01:40 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 08:02:05 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 08:02:06 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 08:02:09 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 08:02:18 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 08:02:47 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 08:02:52 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 08:02:52 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 08:02:53 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 08:02:54 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 08:02:55 GMT
USER 8983
# Thu, 02 Mar 2023 08:02:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 08:02:56 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bf781428c54e99ccbf1268ef9774419ef70853536b11e51069c5ce69a81411`  
		Last Modified: Thu, 02 Mar 2023 04:17:41 GMT  
		Size: 17.6 MB (17577844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ae18692519ea6e19ae7b568af3c2b799d01a619b39daa6d2c0c6b58c9fca3`  
		Last Modified: Thu, 02 Mar 2023 04:20:36 GMT  
		Size: 42.1 MB (42063930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0838e4d8dd76f317b7f4d58ffee9c408c332049036c753c2abdce5150a06748`  
		Last Modified: Thu, 02 Mar 2023 04:20:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e441ff279834714f67bb64c7b695faa8f1960da4a3f2756d789bc36205f3c1b9`  
		Last Modified: Thu, 02 Mar 2023 08:04:42 GMT  
		Size: 5.8 MB (5774125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95ee580ffd0bac0d4d4b7d1f75fc7871f5a99ce51f7a069aee29365bfa9451e`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacd7ad985504adce4c895b47011cfc11c425432aecba2af493ffda95b12997a`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:facf7fbd26499d791476a965c764fad71512ae2511e311428281371a608e41bc`  
		Last Modified: Thu, 02 Mar 2023 08:04:58 GMT  
		Size: 218.3 MB (218328234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811c7ecc40254961fbc4166e06df935d6a585b78b37ffdb467324fa3312f2b62`  
		Last Modified: Thu, 02 Mar 2023 08:04:41 GMT  
		Size: 6.3 KB (6313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8.11.2-slim` - linux; s390x

```console
$ docker pull solr@sha256:46225deee69ac78aa85f2b3d3972f1d87166c5f14a8cc48d1df86801fc572217
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306655846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3848b5e68ff932c3930fbbd9c046067ccf839eb6c254664c1fdbe7f6bce47bef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 02:26:33 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:26:34 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Thu, 02 Mar 2023 02:27:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='89bc6e93d48a37a5eff7ec5afa515c60eb3369d106d1736f5e845b3dcf8fb72c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='949482ac232e756f342de6a8592d56b58803e10d3956abff14c4958e711a0b7c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='df32e80d5b6db60a1ed9ed04eaf267eaf17835ed2ae2c1708d8d94328c03a0a5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c07df5081f78021bed0d169622e470ebd4a4525a45f84192a52580ddb912959b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='0e7b196ef8603ac3d38caaf7768b7b0a3c613d60e15a6511bcfb2c894b609e99';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 02:27:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 19:33:13 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 02 Mar 2023 19:33:13 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 02 Mar 2023 19:33:13 GMT
ARG SOLR_VERSION=8.11.2
# Thu, 02 Mar 2023 19:33:13 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 19:33:14 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 19:33:21 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 02 Mar 2023 19:33:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 02 Mar 2023 19:33:23 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 19:33:30 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 02 Mar 2023 19:33:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 02 Mar 2023 19:34:02 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Thu, 02 Mar 2023 19:34:02 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 19:34:03 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 19:34:03 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 19:34:03 GMT
USER 8983
# Thu, 02 Mar 2023 19:34:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:34:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d6ac74ab42247b9491b6986614b9868ce755dc1c84611543400690873aa73416`  
		Last Modified: Thu, 02 Mar 2023 02:22:20 GMT  
		Size: 27.0 MB (27016384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec20b82de555147dd038f63cd5be763d32cf5bd0e6a05afbaae491bfbafed5a1`  
		Last Modified: Thu, 02 Mar 2023 02:33:31 GMT  
		Size: 16.0 MB (16033099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879782d8f5dfc0f56a537f8a8ba4e15cef875216def8cdc8dde3f6e7a0e17271`  
		Last Modified: Thu, 02 Mar 2023 02:34:19 GMT  
		Size: 40.5 MB (40536858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183e8ef00bdf3c3ec288c92da3d626a4e0d27b00f537fed2b1714ac8b0e67b1`  
		Last Modified: Thu, 02 Mar 2023 02:34:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02dbc85bc5a9dd6a28499df5fe4cddbc082a0fe97e01e7b0ff65b652fe16f86`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 4.7 MB (4727022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fed773d0f1382ecb00b942174d4a5c236671c1918d8a7fe86399e858a4ff45`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0340d8812b788b38da33f58f47173802a2162d85b12af65076aca6036bdae8fb`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9dbbe7da60b5a9325818981f69392935389afdecb14a1cfcb60eecfb92c797`  
		Last Modified: Thu, 02 Mar 2023 19:35:41 GMT  
		Size: 218.3 MB (218328221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a46632aa59e9ccf2c0c6cefab6d1679d5a834f38062dae5da7e4cb035e033d`  
		Last Modified: Thu, 02 Mar 2023 19:35:31 GMT  
		Size: 6.3 KB (6307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:9`

```console
$ docker pull solr@sha256:83e18655f0f423379c2607cbad94fda486b1b3dcad6066defca8c18d6cdf75b3
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
$ docker pull solr@sha256:7ae731cf7ade88408e539274648e4bf7b30ea10d54369bf0615b5bb5389e96db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330942272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb94e6b98a98caf4732577e39d235cc284e6e40db07df661911b79a24d931760`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:03:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:04:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:04:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 10:03:54 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 10:03:54 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 10:03:54 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 10:04:19 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 02 Mar 2023 10:04:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 10:04:21 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 10:04:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 10:04:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 10:04:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 10:04:31 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 10:04:31 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 10:04:31 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 10:04:31 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 10:04:31 GMT
USER 8983
# Thu, 02 Mar 2023 10:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:04:31 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedde91f7fda56da911564f824cff490cec019cf9146119947787937b628e7e9`  
		Last Modified: Thu, 02 Mar 2023 04:10:16 GMT  
		Size: 20.1 MB (20091922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d255ae1b0e629f899b27cf436e936ab95457801ac0a81a67d69463b74cd06ec2`  
		Last Modified: Thu, 02 Mar 2023 04:11:18 GMT  
		Size: 46.9 MB (46936990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af911ce721372f9284a012407b5c6205e056dc377a5c4457069b43207ffa6d8`  
		Last Modified: Thu, 02 Mar 2023 04:11:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4a05be9271679d4b2d626e8e7bd946145213ce56b5b36ffa6b4a8bf9ca8ec`  
		Last Modified: Thu, 02 Mar 2023 10:24:07 GMT  
		Size: 233.7 MB (233741006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8596a8fd15162ffe7b169c0904392684c3728c7039c1e716c64b1cef496c483`  
		Last Modified: Thu, 02 Mar 2023 10:23:56 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1445a693048ede3241afc393c9796f6811abfbd63ad734c9fb558d41d55bf5`  
		Last Modified: Thu, 02 Mar 2023 10:23:56 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fafdf0f6dacb75209cc6ddf890dd7ac9742fe16e8b42deb0d87e9e15fb4d63`  
		Last Modified: Thu, 02 Mar 2023 10:23:56 GMT  
		Size: 8.1 KB (8083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442192fc13ee950d548797565452341f99ab8825e2b303620561dddc0c646db`  
		Last Modified: Thu, 02 Mar 2023 10:23:57 GMT  
		Size: 1.6 MB (1581596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9` - linux; arm variant v7

```console
$ docker pull solr@sha256:87c2c91166b2effd7b5c252d06181f1e89874156003048505800ab3f26dce775
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323206815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5157911afde46379c02997af2aa4fac83892ab68a6bfed5e0779f98fca7591`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:45:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:48:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:48:47 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:50:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:50:01 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:44:24 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 16 Mar 2023 04:44:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 04:44:26 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 04:44:26 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 04:44:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 04:44:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 04:44:36 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 04:44:36 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 04:44:36 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 04:44:36 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 04:44:36 GMT
USER 8983
# Thu, 16 Mar 2023 04:44:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 04:44:36 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1244137e4b88ca1866cf46370a384651ad01ecf13089022ced8c41a497b37663`  
		Last Modified: Thu, 16 Mar 2023 02:55:57 GMT  
		Size: 19.5 MB (19462442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bc0431536f0b89ee088a790995dd293ec25d3688eb9ca73359b82336dd8768`  
		Last Modified: Thu, 16 Mar 2023 02:57:05 GMT  
		Size: 44.5 MB (44529856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbabb516d40e0733a3335db3a801c1d210be0e2c9afd8adfd32db5c4cd9d518c`  
		Last Modified: Thu, 16 Mar 2023 02:56:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162837bfbbd64039ee4257e98c01d2ee735e529ba6c3db116879af03d10394ff`  
		Last Modified: Thu, 16 Mar 2023 04:47:30 GMT  
		Size: 233.2 MB (233220701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3741ea3b9c8f232fc4341c907a62fd01ffbdb1aa6d876d0cd2b00952d9dc4f27`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 4.2 KB (4224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d674ecb316d5958afe3ed25d77276f9b318841fa534a99bc3f07a4458004b`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79817a7b907cfac994784d46ffb2efba1ca1bbde59ab25736bf121ff6cf7d16`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 8.1 KB (8088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cd4541998525c86de76ce4b4e78a588dbcaba6f0de0c85d2ab715c6cc2250e`  
		Last Modified: Thu, 16 Mar 2023 04:47:18 GMT  
		Size: 1.4 MB (1394644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:5fb2c69ebadcdc76017fc3a76326d24b45e0e57bcc239fc3a1c88f37f2206618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329617407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a621b7f499b8a7e163383c98308d68a3ca9118674c4ff5be9134373854336693`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:51:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:54:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:54:31 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:55:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:55:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:52 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 06:14:54 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 06:14:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 06:14:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 06:14:56 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 06:15:03 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 06:15:03 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 06:15:03 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 06:15:03 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 06:15:03 GMT
USER 8983
# Thu, 16 Mar 2023 06:15:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:15:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f091a26bf16cf9bb9b5741a2f8b70047ee293b3a06b86283bea82ea46a9343a2`  
		Last Modified: Thu, 16 Mar 2023 02:00:21 GMT  
		Size: 20.8 MB (20810964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b693cb82e58b3095ebe84d13ae1a3782dd356f500a91d5a61a47e8235d6e2a67`  
		Last Modified: Thu, 16 Mar 2023 02:01:11 GMT  
		Size: 46.4 MB (46422408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d34498a6f57f8c837ca795570cb62efb66090dab255070ba11325965a0200`  
		Last Modified: Thu, 16 Mar 2023 02:01:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0484642c6ee51824c667f3e27f52270960e3c92c69bc7bfa7ab2f782763fddbd`  
		Last Modified: Thu, 16 Mar 2023 06:17:19 GMT  
		Size: 233.7 MB (233731740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d5eb156f2c791d6c94fa684d3c306e30c0060b7092c019d543a6d1852a61ea`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 4.3 KB (4328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e44d81a875819e3b33e6276257dfa34ff3fee5f4902c09c68a9a3947261064`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af30bf8591fec4083df823499a619bb2721cd6706e16b24f875198b29d551d3`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 8.1 KB (8086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab9e27d15fb1977ad5d628a5a3a00c2e7654d73d672edcd6fab2e1f282fe9c3`  
		Last Modified: Thu, 16 Mar 2023 06:17:11 GMT  
		Size: 1.4 MB (1443341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9` - linux; ppc64le

```console
$ docker pull solr@sha256:a1a69fd4bbdce4625f7837b11b1952be0acc8ad0e5691b614cdfdf382825a79c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338360960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273cc069c12a97e236bf1acf088a6f61503a29182993e85dc6a2112857da0650`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:03:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:09:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:09:28 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:11:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:11:43 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 07:57:46 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 02 Mar 2023 07:57:46 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 02 Mar 2023 07:57:46 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 02 Mar 2023 07:57:47 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 07:57:47 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 07:57:48 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 07:57:49 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 07:57:49 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 07:58:46 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 07:58:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 07:58:51 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 07:58:52 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 07:58:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 07:58:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 07:58:55 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 07:58:56 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 02 Mar 2023 07:58:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 07:58:57 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 07:58:58 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 07:59:00 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 07:59:02 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 07:59:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 07:59:17 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 07:59:18 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 07:59:19 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 07:59:20 GMT
USER 8983
# Thu, 02 Mar 2023 07:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:59:21 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcfd4c29e2858c629cdac7eee60bc7ba8dbd107ea7da4bb03b547506c38308e`  
		Last Modified: Thu, 02 Mar 2023 04:21:16 GMT  
		Size: 22.1 MB (22061782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb82256c20da7e07eaa4b9538f7c2b25e0823298b196b10b8d4cc0b99bb0b94`  
		Last Modified: Thu, 02 Mar 2023 04:22:44 GMT  
		Size: 46.8 MB (46780912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3ce9b4e4142f138693e5dd2bd9a282c82a6963375ebe137fba2ed271e46671`  
		Last Modified: Thu, 02 Mar 2023 04:22:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d986be7d3c9ab324621927aec65f9fdfa3b082f68680d6c6e406bd7328ead5f`  
		Last Modified: Thu, 02 Mar 2023 08:03:53 GMT  
		Size: 234.6 MB (234601089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347ffb373d6504149a76986fd243e6988db6deddde6ebaa33c51549a38eb6cf2`  
		Last Modified: Thu, 02 Mar 2023 08:03:33 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975892b8586cde02378134e1e956ba93deb4a0b519be943ccf87ef443e1b70af`  
		Last Modified: Thu, 02 Mar 2023 08:03:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5d01fecfd669830cd0ac0beb0d2f5fe801f8abb743ec2180ab287f69881060`  
		Last Modified: Thu, 02 Mar 2023 08:03:33 GMT  
		Size: 8.1 KB (8092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d4ab2e2e721ee0101a12b9a3c535eb75392c6c1a2c3ef78140cd647e82870`  
		Last Modified: Thu, 02 Mar 2023 08:03:34 GMT  
		Size: 1.6 MB (1604030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9` - linux; s390x

```console
$ docker pull solr@sha256:eff2d2656441173f360d5e3634c57ff9f29f53d4b1324f923c0dc67fef5f4dc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325448846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39edd1c02dba77220e37814fd47d672811b28086a85635337f4f20f5d98c9aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 02:28:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:28:26 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 02:29:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 02:29:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 19:30:19 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 02 Mar 2023 19:30:19 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 02 Mar 2023 19:30:19 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 02 Mar 2023 19:30:20 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 19:30:21 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 19:30:21 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 19:30:21 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 19:30:22 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 19:31:02 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 19:31:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 19:31:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 19:31:17 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 19:31:17 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 19:31:17 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 19:31:18 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 19:31:19 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 02 Mar 2023 19:31:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 19:31:19 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 19:31:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 19:31:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 19:31:23 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 19:31:29 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 19:31:29 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 19:31:29 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 19:31:30 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 19:31:30 GMT
USER 8983
# Thu, 02 Mar 2023 19:31:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:31:30 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d6ac74ab42247b9491b6986614b9868ce755dc1c84611543400690873aa73416`  
		Last Modified: Thu, 02 Mar 2023 02:22:20 GMT  
		Size: 27.0 MB (27016384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c998886554c68bd1179c9b0681699894e6a218a2f8938bc21ff5946911711b9f`  
		Last Modified: Thu, 02 Mar 2023 02:34:49 GMT  
		Size: 19.5 MB (19526654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70257de6ab5ab2c547fb3a6f33eed2a87916d198595947517941463e6375c4de`  
		Last Modified: Thu, 02 Mar 2023 02:35:32 GMT  
		Size: 43.7 MB (43739796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f11339ff9a469ece5c3c80559c9a7e5a683363b6831a2c472000f08938f0a`  
		Last Modified: Thu, 02 Mar 2023 02:35:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2711b71f04831e4899a5ad0c74d93214103e744afbba172e243f1751ec69fe`  
		Last Modified: Thu, 02 Mar 2023 19:35:01 GMT  
		Size: 233.7 MB (233657272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c59a45b188ab6ea12f698f22a2607d81439f247fbf86f11a7317dbfb959d29f`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20fb411eb8f75d9bf9d9085bb56ad644952e6bc9abd1fb4bc5fd32f226e8013`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfa5bf288d7135799a3012bd7a3d2a1d04174e5df83756460e4d996bb74b583`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 8.1 KB (8083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f841e66895f7471899ddcc0d3eee90def05320cbd1311576e68c6a11fa97eb7e`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 1.5 MB (1495950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:9.0`

```console
$ docker pull solr@sha256:3da609ef91203254a1807bf6fa1089cf193ab1f638aaefde798d133a21ad2560
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
$ docker pull solr@sha256:2c267ea705bf74acb5c208fc0b6b6d7f315cc60905ecae9d696a0d3ead9ff42e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324863094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc73b429d3c50e431e149e689eafeaace4764bbd6315e5bc272012247777ca27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:03:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:04:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:04:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_VERSION=9.0.0
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 10:22:28 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 10:22:29 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 10:22:29 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 10:22:29 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 10:22:29 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 10:22:29 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 10:22:29 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 10:22:30 GMT
LABEL org.opencontainers.image.version=9.0.0
# Thu, 02 Mar 2023 10:22:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 10:22:30 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 10:22:30 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 10:22:31 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 10:22:31 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 10:22:37 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 10:22:37 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 10:22:37 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 10:22:37 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 10:22:37 GMT
USER solr
# Thu, 02 Mar 2023 10:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:22:37 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedde91f7fda56da911564f824cff490cec019cf9146119947787937b628e7e9`  
		Last Modified: Thu, 02 Mar 2023 04:10:16 GMT  
		Size: 20.1 MB (20091922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d255ae1b0e629f899b27cf436e936ab95457801ac0a81a67d69463b74cd06ec2`  
		Last Modified: Thu, 02 Mar 2023 04:11:18 GMT  
		Size: 46.9 MB (46936990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af911ce721372f9284a012407b5c6205e056dc377a5c4457069b43207ffa6d8`  
		Last Modified: Thu, 02 Mar 2023 04:11:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42be9f71fbfe23e6253b35582ca07f719ca113c874417d943f6d1a76103aa02a`  
		Last Modified: Thu, 02 Mar 2023 10:24:31 GMT  
		Size: 227.7 MB (227661989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa98e9a32849271a659501ca6e10520c04ac8266feee678fbcdfba960341537b`  
		Last Modified: Thu, 02 Mar 2023 10:24:20 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399a3fb961c92efa916998eaae94f189e32a7b8b30a27d0427a44e1b20a90e9c`  
		Last Modified: Thu, 02 Mar 2023 10:24:20 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a7beeda4978690e0ea7189363cd076260911bbf2f3050d21e8604c7d22a1bd`  
		Last Modified: Thu, 02 Mar 2023 10:24:20 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaeee5c9391f18e699479d217f3c3c1d6e52901d798c2f5a7942dfd14d4967a`  
		Last Modified: Thu, 02 Mar 2023 10:24:21 GMT  
		Size: 1.6 MB (1581618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0` - linux; arm variant v7

```console
$ docker pull solr@sha256:e2320bad4bb477c8e2841820802e72c9520b7247acf1a96bf7677dbfef9b5b99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317126582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c1415765abbfa86163a448b70e989bc7e7b57e18705914adbf645d432512c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:45:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:48:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:48:47 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:50:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:50:01 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:44:46 GMT
ARG SOLR_VERSION=9.0.0
# Thu, 16 Mar 2023 04:44:46 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Thu, 16 Mar 2023 04:44:46 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 16 Mar 2023 04:44:46 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 04:44:47 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 04:44:47 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 16 Mar 2023 04:44:47 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 16 Mar 2023 04:44:47 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 16 Mar 2023 04:45:32 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 04:45:33 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 04:45:33 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 04:45:33 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 04:45:33 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 04:45:33 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 04:45:33 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 04:45:33 GMT
LABEL org.opencontainers.image.version=9.0.0
# Thu, 16 Mar 2023 04:45:34 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 04:45:34 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 04:45:34 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 04:45:35 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 04:45:35 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 04:45:39 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 04:45:39 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 04:45:39 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 04:45:39 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 04:45:39 GMT
USER solr
# Thu, 16 Mar 2023 04:45:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 04:45:40 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1244137e4b88ca1866cf46370a384651ad01ecf13089022ced8c41a497b37663`  
		Last Modified: Thu, 16 Mar 2023 02:55:57 GMT  
		Size: 19.5 MB (19462442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bc0431536f0b89ee088a790995dd293ec25d3688eb9ca73359b82336dd8768`  
		Last Modified: Thu, 16 Mar 2023 02:57:05 GMT  
		Size: 44.5 MB (44529856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbabb516d40e0733a3335db3a801c1d210be0e2c9afd8adfd32db5c4cd9d518c`  
		Last Modified: Thu, 16 Mar 2023 02:56:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1892a6fb7f06c37be83ca6c873761525e642f6fb95a2eb4e04fb1aebc8c1e45d`  
		Last Modified: Thu, 16 Mar 2023 04:48:00 GMT  
		Size: 227.1 MB (227140607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c53758671be9b13735099a72cfee046cdf4e722bce4d6999f1a99e9d5d99447`  
		Last Modified: Thu, 16 Mar 2023 04:47:47 GMT  
		Size: 4.2 KB (4221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b5d7777645acbbd93041e16a624e185a6798d2c218856595ef840159ff5b6a`  
		Last Modified: Thu, 16 Mar 2023 04:47:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b2d5bdf418023597743c0bd7b1ce3d1b35096a88b6f64a01e327b926c5bd3e`  
		Last Modified: Thu, 16 Mar 2023 04:47:47 GMT  
		Size: 7.9 KB (7901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef7347b1cd1b42891c7823f49cfe1328047ec5d13a21a127b2e8edd041a5890`  
		Last Modified: Thu, 16 Mar 2023 04:47:47 GMT  
		Size: 1.4 MB (1394694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:685a2a29882753fb62e471501b02a9ae2c60cd114cb9ee559dc8e9e969202fe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 MB (323535575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc038d5fe33819c350458eb1528a67836d447faa943aad49ba6059121953360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:51:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:54:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:54:31 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:55:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:55:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_VERSION=9.0.0
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 16 Mar 2023 06:15:45 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.version=9.0.0
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 06:15:47 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 06:15:48 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 06:15:48 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 06:15:49 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 06:15:52 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 06:15:52 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 06:15:53 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 06:15:53 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 06:15:53 GMT
USER solr
# Thu, 16 Mar 2023 06:15:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:15:53 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f091a26bf16cf9bb9b5741a2f8b70047ee293b3a06b86283bea82ea46a9343a2`  
		Last Modified: Thu, 16 Mar 2023 02:00:21 GMT  
		Size: 20.8 MB (20810964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b693cb82e58b3095ebe84d13ae1a3782dd356f500a91d5a61a47e8235d6e2a67`  
		Last Modified: Thu, 16 Mar 2023 02:01:11 GMT  
		Size: 46.4 MB (46422408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d34498a6f57f8c837ca795570cb62efb66090dab255070ba11325965a0200`  
		Last Modified: Thu, 16 Mar 2023 02:01:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691359bc5838741f19181dbd60138d1b671f9884ad2003835a9ebc2f6be8aee1`  
		Last Modified: Thu, 16 Mar 2023 06:17:41 GMT  
		Size: 227.7 MB (227650132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe705ddfa6148896753f492b1bbf7fb69ab9274c2acb8810800adf237580931d`  
		Last Modified: Thu, 16 Mar 2023 06:17:33 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0112133b8e55b2ee8432a9d5ed997fad8568df2a286780965ec6ae452b2b3035`  
		Last Modified: Thu, 16 Mar 2023 06:17:32 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa58eee789529ad94c7e362ec15c9df1f062b5eb87925f1c6933f65bb07ce87`  
		Last Modified: Thu, 16 Mar 2023 06:17:33 GMT  
		Size: 7.9 KB (7906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225bb3df111e2541e5e5a013ce7082f568487db651388700257042012351992a`  
		Last Modified: Thu, 16 Mar 2023 06:17:33 GMT  
		Size: 1.4 MB (1443295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0` - linux; ppc64le

```console
$ docker pull solr@sha256:4bda5c81c1334cdb0cb01e67bbdfc23e1942a540652711c171ec0ab4d3785fe0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332280714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aaede92a2de691a22ee1804bcaf7271b06433047b30956f9848821c8f746318`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:03:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:09:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:09:28 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:11:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:11:43 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 07:59:26 GMT
ARG SOLR_VERSION=9.0.0
# Thu, 02 Mar 2023 07:59:28 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Thu, 02 Mar 2023 07:59:28 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 02 Mar 2023 07:59:29 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 07:59:29 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 07:59:30 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 07:59:30 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 07:59:30 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 08:00:47 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 08:00:52 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 08:00:53 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 08:00:53 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 08:00:54 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 08:00:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 08:00:55 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 08:00:56 GMT
LABEL org.opencontainers.image.version=9.0.0
# Thu, 02 Mar 2023 08:00:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 08:00:57 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 08:01:00 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 08:01:01 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 08:01:03 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 08:01:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 08:01:15 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 08:01:16 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 08:01:17 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 08:01:17 GMT
USER solr
# Thu, 02 Mar 2023 08:01:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 08:01:18 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcfd4c29e2858c629cdac7eee60bc7ba8dbd107ea7da4bb03b547506c38308e`  
		Last Modified: Thu, 02 Mar 2023 04:21:16 GMT  
		Size: 22.1 MB (22061782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb82256c20da7e07eaa4b9538f7c2b25e0823298b196b10b8d4cc0b99bb0b94`  
		Last Modified: Thu, 02 Mar 2023 04:22:44 GMT  
		Size: 46.8 MB (46780912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3ce9b4e4142f138693e5dd2bd9a282c82a6963375ebe137fba2ed271e46671`  
		Last Modified: Thu, 02 Mar 2023 04:22:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f270fbf51c2fe092af0482dd3c68d36db8342f52aef209526545a0572ef4c3`  
		Last Modified: Thu, 02 Mar 2023 08:04:28 GMT  
		Size: 228.5 MB (228521027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4529f4a91cfbae65f76210cfa1cf02fcb44b01f6e1286d8cebe6445410cd64`  
		Last Modified: Thu, 02 Mar 2023 08:04:10 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8c477aa4958ef905b416bd3ff5d0af2716a2c3e66727d42450952e849f0c12`  
		Last Modified: Thu, 02 Mar 2023 08:04:10 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862f77225f6d1ac6fd2e56fb5a999804bd6f05a9f9e3b4e3b24209d5c56ef757`  
		Last Modified: Thu, 02 Mar 2023 08:04:10 GMT  
		Size: 7.9 KB (7903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733a2ccd68c1151b86bcd294ca0768e5f04334b47b89ad54d2dae3e1277fc66`  
		Last Modified: Thu, 02 Mar 2023 08:04:10 GMT  
		Size: 1.6 MB (1604038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0` - linux; s390x

```console
$ docker pull solr@sha256:f1f5daa741c3929a48f6b7c817c5b545b5f3cf03bcc700aee0ce3c459f719ed0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.4 MB (319367147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1b7af1b7303473b20a91d538841a2355bf6f5a39d0d81509a7829f631ffcc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 02:28:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:28:26 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 02:29:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 02:29:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 19:31:39 GMT
ARG SOLR_VERSION=9.0.0
# Thu, 02 Mar 2023 19:31:39 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Thu, 02 Mar 2023 19:31:39 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 02 Mar 2023 19:31:40 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 19:31:40 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 19:31:40 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 19:31:40 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 19:31:41 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 19:32:24 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 19:32:32 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 19:32:33 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 19:32:34 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 19:32:34 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 19:32:35 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 19:32:35 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 19:32:36 GMT
LABEL org.opencontainers.image.version=9.0.0
# Thu, 02 Mar 2023 19:32:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 19:32:37 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 19:32:39 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 19:32:41 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 19:32:42 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 19:32:50 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 19:32:51 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 19:32:52 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 19:32:53 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 19:32:53 GMT
USER solr
# Thu, 02 Mar 2023 19:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:32:55 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:d6ac74ab42247b9491b6986614b9868ce755dc1c84611543400690873aa73416`  
		Last Modified: Thu, 02 Mar 2023 02:22:20 GMT  
		Size: 27.0 MB (27016384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c998886554c68bd1179c9b0681699894e6a218a2f8938bc21ff5946911711b9f`  
		Last Modified: Thu, 02 Mar 2023 02:34:49 GMT  
		Size: 19.5 MB (19526654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70257de6ab5ab2c547fb3a6f33eed2a87916d198595947517941463e6375c4de`  
		Last Modified: Thu, 02 Mar 2023 02:35:32 GMT  
		Size: 43.7 MB (43739796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f11339ff9a469ece5c3c80559c9a7e5a683363b6831a2c472000f08938f0a`  
		Last Modified: Thu, 02 Mar 2023 02:35:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2514e2e08ebc6f2dbb4a3518ba4ff5c135b9aa52bef6b6f5d5311931588bce5`  
		Last Modified: Thu, 02 Mar 2023 19:35:23 GMT  
		Size: 227.6 MB (227575716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f22db5a1015c292373f01fbdf1df1fe363f75d82b54fee851521d036663468`  
		Last Modified: Thu, 02 Mar 2023 19:35:14 GMT  
		Size: 4.3 KB (4334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8070e9c6cc12d60d872182b3dd376444638c4cb0821994c00954a1c26594da71`  
		Last Modified: Thu, 02 Mar 2023 19:35:14 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87f63cc79b508ec102258b6770631ab0167e36c54a44431b42a4e3fab68d810`  
		Last Modified: Thu, 02 Mar 2023 19:35:13 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfffe0292e14a314828a3b40dbec430a7aaaea9ef1cc7f49ddf610ac58e88b3e`  
		Last Modified: Thu, 02 Mar 2023 19:35:14 GMT  
		Size: 1.5 MB (1495976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:9.0.0`

```console
$ docker pull solr@sha256:3da609ef91203254a1807bf6fa1089cf193ab1f638aaefde798d133a21ad2560
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
$ docker pull solr@sha256:2c267ea705bf74acb5c208fc0b6b6d7f315cc60905ecae9d696a0d3ead9ff42e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324863094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc73b429d3c50e431e149e689eafeaace4764bbd6315e5bc272012247777ca27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:03:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:04:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:04:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_VERSION=9.0.0
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 10:04:34 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 10:22:28 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 10:22:29 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 10:22:29 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 10:22:29 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 10:22:29 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 10:22:29 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 10:22:29 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 10:22:30 GMT
LABEL org.opencontainers.image.version=9.0.0
# Thu, 02 Mar 2023 10:22:30 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 10:22:30 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 10:22:30 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 10:22:31 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 10:22:31 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 10:22:37 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 10:22:37 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 10:22:37 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 10:22:37 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 10:22:37 GMT
USER solr
# Thu, 02 Mar 2023 10:22:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:22:37 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedde91f7fda56da911564f824cff490cec019cf9146119947787937b628e7e9`  
		Last Modified: Thu, 02 Mar 2023 04:10:16 GMT  
		Size: 20.1 MB (20091922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d255ae1b0e629f899b27cf436e936ab95457801ac0a81a67d69463b74cd06ec2`  
		Last Modified: Thu, 02 Mar 2023 04:11:18 GMT  
		Size: 46.9 MB (46936990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af911ce721372f9284a012407b5c6205e056dc377a5c4457069b43207ffa6d8`  
		Last Modified: Thu, 02 Mar 2023 04:11:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42be9f71fbfe23e6253b35582ca07f719ca113c874417d943f6d1a76103aa02a`  
		Last Modified: Thu, 02 Mar 2023 10:24:31 GMT  
		Size: 227.7 MB (227661989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa98e9a32849271a659501ca6e10520c04ac8266feee678fbcdfba960341537b`  
		Last Modified: Thu, 02 Mar 2023 10:24:20 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399a3fb961c92efa916998eaae94f189e32a7b8b30a27d0427a44e1b20a90e9c`  
		Last Modified: Thu, 02 Mar 2023 10:24:20 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a7beeda4978690e0ea7189363cd076260911bbf2f3050d21e8604c7d22a1bd`  
		Last Modified: Thu, 02 Mar 2023 10:24:20 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaeee5c9391f18e699479d217f3c3c1d6e52901d798c2f5a7942dfd14d4967a`  
		Last Modified: Thu, 02 Mar 2023 10:24:21 GMT  
		Size: 1.6 MB (1581618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0.0` - linux; arm variant v7

```console
$ docker pull solr@sha256:e2320bad4bb477c8e2841820802e72c9520b7247acf1a96bf7677dbfef9b5b99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317126582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c1415765abbfa86163a448b70e989bc7e7b57e18705914adbf645d432512c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:45:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:48:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:48:47 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:50:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:50:01 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:44:46 GMT
ARG SOLR_VERSION=9.0.0
# Thu, 16 Mar 2023 04:44:46 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Thu, 16 Mar 2023 04:44:46 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 16 Mar 2023 04:44:46 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 04:44:47 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 04:44:47 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 16 Mar 2023 04:44:47 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 16 Mar 2023 04:44:47 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 16 Mar 2023 04:45:32 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 04:45:33 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 04:45:33 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 04:45:33 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 04:45:33 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 04:45:33 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 04:45:33 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 04:45:33 GMT
LABEL org.opencontainers.image.version=9.0.0
# Thu, 16 Mar 2023 04:45:34 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 04:45:34 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 04:45:34 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 04:45:35 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 04:45:35 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 04:45:39 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 04:45:39 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 04:45:39 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 04:45:39 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 04:45:39 GMT
USER solr
# Thu, 16 Mar 2023 04:45:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 04:45:40 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1244137e4b88ca1866cf46370a384651ad01ecf13089022ced8c41a497b37663`  
		Last Modified: Thu, 16 Mar 2023 02:55:57 GMT  
		Size: 19.5 MB (19462442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bc0431536f0b89ee088a790995dd293ec25d3688eb9ca73359b82336dd8768`  
		Last Modified: Thu, 16 Mar 2023 02:57:05 GMT  
		Size: 44.5 MB (44529856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbabb516d40e0733a3335db3a801c1d210be0e2c9afd8adfd32db5c4cd9d518c`  
		Last Modified: Thu, 16 Mar 2023 02:56:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1892a6fb7f06c37be83ca6c873761525e642f6fb95a2eb4e04fb1aebc8c1e45d`  
		Last Modified: Thu, 16 Mar 2023 04:48:00 GMT  
		Size: 227.1 MB (227140607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c53758671be9b13735099a72cfee046cdf4e722bce4d6999f1a99e9d5d99447`  
		Last Modified: Thu, 16 Mar 2023 04:47:47 GMT  
		Size: 4.2 KB (4221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b5d7777645acbbd93041e16a624e185a6798d2c218856595ef840159ff5b6a`  
		Last Modified: Thu, 16 Mar 2023 04:47:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b2d5bdf418023597743c0bd7b1ce3d1b35096a88b6f64a01e327b926c5bd3e`  
		Last Modified: Thu, 16 Mar 2023 04:47:47 GMT  
		Size: 7.9 KB (7901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef7347b1cd1b42891c7823f49cfe1328047ec5d13a21a127b2e8edd041a5890`  
		Last Modified: Thu, 16 Mar 2023 04:47:47 GMT  
		Size: 1.4 MB (1394694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0.0` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:685a2a29882753fb62e471501b02a9ae2c60cd114cb9ee559dc8e9e969202fe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 MB (323535575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc038d5fe33819c350458eb1528a67836d447faa943aad49ba6059121953360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:51:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:54:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:54:31 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:55:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:55:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_VERSION=9.0.0
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 16 Mar 2023 06:15:07 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 16 Mar 2023 06:15:45 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.version=9.0.0
# Thu, 16 Mar 2023 06:15:47 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 06:15:47 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 06:15:48 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 06:15:48 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 06:15:49 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 06:15:52 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 06:15:52 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 06:15:53 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 06:15:53 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 06:15:53 GMT
USER solr
# Thu, 16 Mar 2023 06:15:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:15:53 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f091a26bf16cf9bb9b5741a2f8b70047ee293b3a06b86283bea82ea46a9343a2`  
		Last Modified: Thu, 16 Mar 2023 02:00:21 GMT  
		Size: 20.8 MB (20810964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b693cb82e58b3095ebe84d13ae1a3782dd356f500a91d5a61a47e8235d6e2a67`  
		Last Modified: Thu, 16 Mar 2023 02:01:11 GMT  
		Size: 46.4 MB (46422408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d34498a6f57f8c837ca795570cb62efb66090dab255070ba11325965a0200`  
		Last Modified: Thu, 16 Mar 2023 02:01:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691359bc5838741f19181dbd60138d1b671f9884ad2003835a9ebc2f6be8aee1`  
		Last Modified: Thu, 16 Mar 2023 06:17:41 GMT  
		Size: 227.7 MB (227650132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe705ddfa6148896753f492b1bbf7fb69ab9274c2acb8810800adf237580931d`  
		Last Modified: Thu, 16 Mar 2023 06:17:33 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0112133b8e55b2ee8432a9d5ed997fad8568df2a286780965ec6ae452b2b3035`  
		Last Modified: Thu, 16 Mar 2023 06:17:32 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa58eee789529ad94c7e362ec15c9df1f062b5eb87925f1c6933f65bb07ce87`  
		Last Modified: Thu, 16 Mar 2023 06:17:33 GMT  
		Size: 7.9 KB (7906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225bb3df111e2541e5e5a013ce7082f568487db651388700257042012351992a`  
		Last Modified: Thu, 16 Mar 2023 06:17:33 GMT  
		Size: 1.4 MB (1443295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0.0` - linux; ppc64le

```console
$ docker pull solr@sha256:4bda5c81c1334cdb0cb01e67bbdfc23e1942a540652711c171ec0ab4d3785fe0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332280714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aaede92a2de691a22ee1804bcaf7271b06433047b30956f9848821c8f746318`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:03:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:09:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:09:28 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:11:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:11:43 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 07:59:26 GMT
ARG SOLR_VERSION=9.0.0
# Thu, 02 Mar 2023 07:59:28 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Thu, 02 Mar 2023 07:59:28 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 02 Mar 2023 07:59:29 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 07:59:29 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 07:59:30 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 07:59:30 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 07:59:30 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 08:00:47 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 08:00:52 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 08:00:53 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 08:00:53 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 08:00:54 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 08:00:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 08:00:55 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 08:00:56 GMT
LABEL org.opencontainers.image.version=9.0.0
# Thu, 02 Mar 2023 08:00:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 08:00:57 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 08:01:00 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 08:01:01 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 08:01:03 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 08:01:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 08:01:15 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 08:01:16 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 08:01:17 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 08:01:17 GMT
USER solr
# Thu, 02 Mar 2023 08:01:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 08:01:18 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcfd4c29e2858c629cdac7eee60bc7ba8dbd107ea7da4bb03b547506c38308e`  
		Last Modified: Thu, 02 Mar 2023 04:21:16 GMT  
		Size: 22.1 MB (22061782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb82256c20da7e07eaa4b9538f7c2b25e0823298b196b10b8d4cc0b99bb0b94`  
		Last Modified: Thu, 02 Mar 2023 04:22:44 GMT  
		Size: 46.8 MB (46780912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3ce9b4e4142f138693e5dd2bd9a282c82a6963375ebe137fba2ed271e46671`  
		Last Modified: Thu, 02 Mar 2023 04:22:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f270fbf51c2fe092af0482dd3c68d36db8342f52aef209526545a0572ef4c3`  
		Last Modified: Thu, 02 Mar 2023 08:04:28 GMT  
		Size: 228.5 MB (228521027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4529f4a91cfbae65f76210cfa1cf02fcb44b01f6e1286d8cebe6445410cd64`  
		Last Modified: Thu, 02 Mar 2023 08:04:10 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8c477aa4958ef905b416bd3ff5d0af2716a2c3e66727d42450952e849f0c12`  
		Last Modified: Thu, 02 Mar 2023 08:04:10 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862f77225f6d1ac6fd2e56fb5a999804bd6f05a9f9e3b4e3b24209d5c56ef757`  
		Last Modified: Thu, 02 Mar 2023 08:04:10 GMT  
		Size: 7.9 KB (7903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733a2ccd68c1151b86bcd294ca0768e5f04334b47b89ad54d2dae3e1277fc66`  
		Last Modified: Thu, 02 Mar 2023 08:04:10 GMT  
		Size: 1.6 MB (1604038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.0.0` - linux; s390x

```console
$ docker pull solr@sha256:f1f5daa741c3929a48f6b7c817c5b545b5f3cf03bcc700aee0ce3c459f719ed0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.4 MB (319367147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1b7af1b7303473b20a91d538841a2355bf6f5a39d0d81509a7829f631ffcc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground","-a","-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 02:28:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:28:26 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 02:29:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 02:29:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 19:31:39 GMT
ARG SOLR_VERSION=9.0.0
# Thu, 02 Mar 2023 19:31:39 GMT
ARG SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5
# Thu, 02 Mar 2023 19:31:39 GMT
ARG SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93
# Thu, 02 Mar 2023 19:31:40 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 19:31:40 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 19:31:40 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 19:31:40 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 19:31:41 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz
# Thu, 02 Mar 2023 19:32:24 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=2;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 19:32:32 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 19:32:33 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 19:32:34 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 19:32:34 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 19:32:35 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 19:32:35 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 19:32:36 GMT
LABEL org.opencontainers.image.version=9.0.0
# Thu, 02 Mar 2023 19:32:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 19:32:37 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 19:32:39 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 19:32:41 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 19:32:42 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 19:32:50 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.0.0/solr-9.0.0.tgz SOLR_KEYS=3558857D1F5754B78C7F8B5A71A45A3D0D8D0B93 SOLR_SHA512=383c6b6f352f2a385ece99b2b0a82e1552430aea65c6c33e5569da422138844192db4e06f58699325af55ee631694e16f836a5bbf8556f86fdeabc0cfa0533d5 SOLR_VERSION=9.0.0
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 19:32:51 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 19:32:52 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 19:32:53 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 19:32:53 GMT
USER solr
# Thu, 02 Mar 2023 19:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:32:55 GMT
CMD ["solr-foreground" "-a" "-XX:CompileCommand=exclude,com.github.benmanes.caffeine.cache.BoundedLocalCache::put"]
```

-	Layers:
	-	`sha256:d6ac74ab42247b9491b6986614b9868ce755dc1c84611543400690873aa73416`  
		Last Modified: Thu, 02 Mar 2023 02:22:20 GMT  
		Size: 27.0 MB (27016384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c998886554c68bd1179c9b0681699894e6a218a2f8938bc21ff5946911711b9f`  
		Last Modified: Thu, 02 Mar 2023 02:34:49 GMT  
		Size: 19.5 MB (19526654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70257de6ab5ab2c547fb3a6f33eed2a87916d198595947517941463e6375c4de`  
		Last Modified: Thu, 02 Mar 2023 02:35:32 GMT  
		Size: 43.7 MB (43739796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f11339ff9a469ece5c3c80559c9a7e5a683363b6831a2c472000f08938f0a`  
		Last Modified: Thu, 02 Mar 2023 02:35:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2514e2e08ebc6f2dbb4a3518ba4ff5c135b9aa52bef6b6f5d5311931588bce5`  
		Last Modified: Thu, 02 Mar 2023 19:35:23 GMT  
		Size: 227.6 MB (227575716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f22db5a1015c292373f01fbdf1df1fe363f75d82b54fee851521d036663468`  
		Last Modified: Thu, 02 Mar 2023 19:35:14 GMT  
		Size: 4.3 KB (4334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8070e9c6cc12d60d872182b3dd376444638c4cb0821994c00954a1c26594da71`  
		Last Modified: Thu, 02 Mar 2023 19:35:14 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87f63cc79b508ec102258b6770631ab0167e36c54a44431b42a4e3fab68d810`  
		Last Modified: Thu, 02 Mar 2023 19:35:13 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfffe0292e14a314828a3b40dbec430a7aaaea9ef1cc7f49ddf610ac58e88b3e`  
		Last Modified: Thu, 02 Mar 2023 19:35:14 GMT  
		Size: 1.5 MB (1495976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:9.1`

```console
$ docker pull solr@sha256:83e18655f0f423379c2607cbad94fda486b1b3dcad6066defca8c18d6cdf75b3
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
$ docker pull solr@sha256:7ae731cf7ade88408e539274648e4bf7b30ea10d54369bf0615b5bb5389e96db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330942272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb94e6b98a98caf4732577e39d235cc284e6e40db07df661911b79a24d931760`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:03:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:04:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:04:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 10:03:54 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 10:03:54 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 10:03:54 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 10:04:19 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 02 Mar 2023 10:04:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 10:04:21 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 10:04:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 10:04:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 10:04:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 10:04:31 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 10:04:31 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 10:04:31 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 10:04:31 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 10:04:31 GMT
USER 8983
# Thu, 02 Mar 2023 10:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:04:31 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedde91f7fda56da911564f824cff490cec019cf9146119947787937b628e7e9`  
		Last Modified: Thu, 02 Mar 2023 04:10:16 GMT  
		Size: 20.1 MB (20091922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d255ae1b0e629f899b27cf436e936ab95457801ac0a81a67d69463b74cd06ec2`  
		Last Modified: Thu, 02 Mar 2023 04:11:18 GMT  
		Size: 46.9 MB (46936990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af911ce721372f9284a012407b5c6205e056dc377a5c4457069b43207ffa6d8`  
		Last Modified: Thu, 02 Mar 2023 04:11:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4a05be9271679d4b2d626e8e7bd946145213ce56b5b36ffa6b4a8bf9ca8ec`  
		Last Modified: Thu, 02 Mar 2023 10:24:07 GMT  
		Size: 233.7 MB (233741006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8596a8fd15162ffe7b169c0904392684c3728c7039c1e716c64b1cef496c483`  
		Last Modified: Thu, 02 Mar 2023 10:23:56 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1445a693048ede3241afc393c9796f6811abfbd63ad734c9fb558d41d55bf5`  
		Last Modified: Thu, 02 Mar 2023 10:23:56 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fafdf0f6dacb75209cc6ddf890dd7ac9742fe16e8b42deb0d87e9e15fb4d63`  
		Last Modified: Thu, 02 Mar 2023 10:23:56 GMT  
		Size: 8.1 KB (8083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442192fc13ee950d548797565452341f99ab8825e2b303620561dddc0c646db`  
		Last Modified: Thu, 02 Mar 2023 10:23:57 GMT  
		Size: 1.6 MB (1581596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1` - linux; arm variant v7

```console
$ docker pull solr@sha256:87c2c91166b2effd7b5c252d06181f1e89874156003048505800ab3f26dce775
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323206815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5157911afde46379c02997af2aa4fac83892ab68a6bfed5e0779f98fca7591`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:45:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:48:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:48:47 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:50:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:50:01 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:44:24 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 16 Mar 2023 04:44:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 04:44:26 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 04:44:26 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 04:44:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 04:44:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 04:44:36 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 04:44:36 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 04:44:36 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 04:44:36 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 04:44:36 GMT
USER 8983
# Thu, 16 Mar 2023 04:44:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 04:44:36 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1244137e4b88ca1866cf46370a384651ad01ecf13089022ced8c41a497b37663`  
		Last Modified: Thu, 16 Mar 2023 02:55:57 GMT  
		Size: 19.5 MB (19462442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bc0431536f0b89ee088a790995dd293ec25d3688eb9ca73359b82336dd8768`  
		Last Modified: Thu, 16 Mar 2023 02:57:05 GMT  
		Size: 44.5 MB (44529856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbabb516d40e0733a3335db3a801c1d210be0e2c9afd8adfd32db5c4cd9d518c`  
		Last Modified: Thu, 16 Mar 2023 02:56:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162837bfbbd64039ee4257e98c01d2ee735e529ba6c3db116879af03d10394ff`  
		Last Modified: Thu, 16 Mar 2023 04:47:30 GMT  
		Size: 233.2 MB (233220701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3741ea3b9c8f232fc4341c907a62fd01ffbdb1aa6d876d0cd2b00952d9dc4f27`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 4.2 KB (4224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d674ecb316d5958afe3ed25d77276f9b318841fa534a99bc3f07a4458004b`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79817a7b907cfac994784d46ffb2efba1ca1bbde59ab25736bf121ff6cf7d16`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 8.1 KB (8088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cd4541998525c86de76ce4b4e78a588dbcaba6f0de0c85d2ab715c6cc2250e`  
		Last Modified: Thu, 16 Mar 2023 04:47:18 GMT  
		Size: 1.4 MB (1394644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:5fb2c69ebadcdc76017fc3a76326d24b45e0e57bcc239fc3a1c88f37f2206618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329617407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a621b7f499b8a7e163383c98308d68a3ca9118674c4ff5be9134373854336693`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:51:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:54:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:54:31 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:55:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:55:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:52 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 06:14:54 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 06:14:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 06:14:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 06:14:56 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 06:15:03 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 06:15:03 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 06:15:03 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 06:15:03 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 06:15:03 GMT
USER 8983
# Thu, 16 Mar 2023 06:15:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:15:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f091a26bf16cf9bb9b5741a2f8b70047ee293b3a06b86283bea82ea46a9343a2`  
		Last Modified: Thu, 16 Mar 2023 02:00:21 GMT  
		Size: 20.8 MB (20810964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b693cb82e58b3095ebe84d13ae1a3782dd356f500a91d5a61a47e8235d6e2a67`  
		Last Modified: Thu, 16 Mar 2023 02:01:11 GMT  
		Size: 46.4 MB (46422408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d34498a6f57f8c837ca795570cb62efb66090dab255070ba11325965a0200`  
		Last Modified: Thu, 16 Mar 2023 02:01:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0484642c6ee51824c667f3e27f52270960e3c92c69bc7bfa7ab2f782763fddbd`  
		Last Modified: Thu, 16 Mar 2023 06:17:19 GMT  
		Size: 233.7 MB (233731740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d5eb156f2c791d6c94fa684d3c306e30c0060b7092c019d543a6d1852a61ea`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 4.3 KB (4328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e44d81a875819e3b33e6276257dfa34ff3fee5f4902c09c68a9a3947261064`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af30bf8591fec4083df823499a619bb2721cd6706e16b24f875198b29d551d3`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 8.1 KB (8086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab9e27d15fb1977ad5d628a5a3a00c2e7654d73d672edcd6fab2e1f282fe9c3`  
		Last Modified: Thu, 16 Mar 2023 06:17:11 GMT  
		Size: 1.4 MB (1443341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1` - linux; ppc64le

```console
$ docker pull solr@sha256:a1a69fd4bbdce4625f7837b11b1952be0acc8ad0e5691b614cdfdf382825a79c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338360960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273cc069c12a97e236bf1acf088a6f61503a29182993e85dc6a2112857da0650`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:03:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:09:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:09:28 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:11:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:11:43 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 07:57:46 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 02 Mar 2023 07:57:46 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 02 Mar 2023 07:57:46 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 02 Mar 2023 07:57:47 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 07:57:47 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 07:57:48 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 07:57:49 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 07:57:49 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 07:58:46 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 07:58:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 07:58:51 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 07:58:52 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 07:58:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 07:58:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 07:58:55 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 07:58:56 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 02 Mar 2023 07:58:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 07:58:57 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 07:58:58 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 07:59:00 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 07:59:02 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 07:59:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 07:59:17 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 07:59:18 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 07:59:19 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 07:59:20 GMT
USER 8983
# Thu, 02 Mar 2023 07:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:59:21 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcfd4c29e2858c629cdac7eee60bc7ba8dbd107ea7da4bb03b547506c38308e`  
		Last Modified: Thu, 02 Mar 2023 04:21:16 GMT  
		Size: 22.1 MB (22061782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb82256c20da7e07eaa4b9538f7c2b25e0823298b196b10b8d4cc0b99bb0b94`  
		Last Modified: Thu, 02 Mar 2023 04:22:44 GMT  
		Size: 46.8 MB (46780912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3ce9b4e4142f138693e5dd2bd9a282c82a6963375ebe137fba2ed271e46671`  
		Last Modified: Thu, 02 Mar 2023 04:22:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d986be7d3c9ab324621927aec65f9fdfa3b082f68680d6c6e406bd7328ead5f`  
		Last Modified: Thu, 02 Mar 2023 08:03:53 GMT  
		Size: 234.6 MB (234601089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347ffb373d6504149a76986fd243e6988db6deddde6ebaa33c51549a38eb6cf2`  
		Last Modified: Thu, 02 Mar 2023 08:03:33 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975892b8586cde02378134e1e956ba93deb4a0b519be943ccf87ef443e1b70af`  
		Last Modified: Thu, 02 Mar 2023 08:03:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5d01fecfd669830cd0ac0beb0d2f5fe801f8abb743ec2180ab287f69881060`  
		Last Modified: Thu, 02 Mar 2023 08:03:33 GMT  
		Size: 8.1 KB (8092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d4ab2e2e721ee0101a12b9a3c535eb75392c6c1a2c3ef78140cd647e82870`  
		Last Modified: Thu, 02 Mar 2023 08:03:34 GMT  
		Size: 1.6 MB (1604030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1` - linux; s390x

```console
$ docker pull solr@sha256:eff2d2656441173f360d5e3634c57ff9f29f53d4b1324f923c0dc67fef5f4dc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325448846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39edd1c02dba77220e37814fd47d672811b28086a85635337f4f20f5d98c9aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 02:28:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:28:26 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 02:29:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 02:29:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 19:30:19 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 02 Mar 2023 19:30:19 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 02 Mar 2023 19:30:19 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 02 Mar 2023 19:30:20 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 19:30:21 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 19:30:21 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 19:30:21 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 19:30:22 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 19:31:02 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 19:31:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 19:31:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 19:31:17 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 19:31:17 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 19:31:17 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 19:31:18 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 19:31:19 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 02 Mar 2023 19:31:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 19:31:19 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 19:31:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 19:31:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 19:31:23 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 19:31:29 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 19:31:29 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 19:31:29 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 19:31:30 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 19:31:30 GMT
USER 8983
# Thu, 02 Mar 2023 19:31:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:31:30 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d6ac74ab42247b9491b6986614b9868ce755dc1c84611543400690873aa73416`  
		Last Modified: Thu, 02 Mar 2023 02:22:20 GMT  
		Size: 27.0 MB (27016384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c998886554c68bd1179c9b0681699894e6a218a2f8938bc21ff5946911711b9f`  
		Last Modified: Thu, 02 Mar 2023 02:34:49 GMT  
		Size: 19.5 MB (19526654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70257de6ab5ab2c547fb3a6f33eed2a87916d198595947517941463e6375c4de`  
		Last Modified: Thu, 02 Mar 2023 02:35:32 GMT  
		Size: 43.7 MB (43739796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f11339ff9a469ece5c3c80559c9a7e5a683363b6831a2c472000f08938f0a`  
		Last Modified: Thu, 02 Mar 2023 02:35:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2711b71f04831e4899a5ad0c74d93214103e744afbba172e243f1751ec69fe`  
		Last Modified: Thu, 02 Mar 2023 19:35:01 GMT  
		Size: 233.7 MB (233657272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c59a45b188ab6ea12f698f22a2607d81439f247fbf86f11a7317dbfb959d29f`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20fb411eb8f75d9bf9d9085bb56ad644952e6bc9abd1fb4bc5fd32f226e8013`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfa5bf288d7135799a3012bd7a3d2a1d04174e5df83756460e4d996bb74b583`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 8.1 KB (8083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f841e66895f7471899ddcc0d3eee90def05320cbd1311576e68c6a11fa97eb7e`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 1.5 MB (1495950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:9.1.1`

```console
$ docker pull solr@sha256:83e18655f0f423379c2607cbad94fda486b1b3dcad6066defca8c18d6cdf75b3
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
$ docker pull solr@sha256:7ae731cf7ade88408e539274648e4bf7b30ea10d54369bf0615b5bb5389e96db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330942272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb94e6b98a98caf4732577e39d235cc284e6e40db07df661911b79a24d931760`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:03:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:04:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:04:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 10:03:54 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 10:03:54 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 10:03:54 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 10:04:19 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 02 Mar 2023 10:04:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 10:04:21 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 10:04:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 10:04:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 10:04:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 10:04:31 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 10:04:31 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 10:04:31 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 10:04:31 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 10:04:31 GMT
USER 8983
# Thu, 02 Mar 2023 10:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:04:31 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedde91f7fda56da911564f824cff490cec019cf9146119947787937b628e7e9`  
		Last Modified: Thu, 02 Mar 2023 04:10:16 GMT  
		Size: 20.1 MB (20091922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d255ae1b0e629f899b27cf436e936ab95457801ac0a81a67d69463b74cd06ec2`  
		Last Modified: Thu, 02 Mar 2023 04:11:18 GMT  
		Size: 46.9 MB (46936990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af911ce721372f9284a012407b5c6205e056dc377a5c4457069b43207ffa6d8`  
		Last Modified: Thu, 02 Mar 2023 04:11:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4a05be9271679d4b2d626e8e7bd946145213ce56b5b36ffa6b4a8bf9ca8ec`  
		Last Modified: Thu, 02 Mar 2023 10:24:07 GMT  
		Size: 233.7 MB (233741006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8596a8fd15162ffe7b169c0904392684c3728c7039c1e716c64b1cef496c483`  
		Last Modified: Thu, 02 Mar 2023 10:23:56 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1445a693048ede3241afc393c9796f6811abfbd63ad734c9fb558d41d55bf5`  
		Last Modified: Thu, 02 Mar 2023 10:23:56 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fafdf0f6dacb75209cc6ddf890dd7ac9742fe16e8b42deb0d87e9e15fb4d63`  
		Last Modified: Thu, 02 Mar 2023 10:23:56 GMT  
		Size: 8.1 KB (8083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442192fc13ee950d548797565452341f99ab8825e2b303620561dddc0c646db`  
		Last Modified: Thu, 02 Mar 2023 10:23:57 GMT  
		Size: 1.6 MB (1581596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1.1` - linux; arm variant v7

```console
$ docker pull solr@sha256:87c2c91166b2effd7b5c252d06181f1e89874156003048505800ab3f26dce775
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323206815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5157911afde46379c02997af2aa4fac83892ab68a6bfed5e0779f98fca7591`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:45:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:48:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:48:47 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:50:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:50:01 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:44:24 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 16 Mar 2023 04:44:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 04:44:26 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 04:44:26 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 04:44:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 04:44:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 04:44:36 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 04:44:36 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 04:44:36 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 04:44:36 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 04:44:36 GMT
USER 8983
# Thu, 16 Mar 2023 04:44:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 04:44:36 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1244137e4b88ca1866cf46370a384651ad01ecf13089022ced8c41a497b37663`  
		Last Modified: Thu, 16 Mar 2023 02:55:57 GMT  
		Size: 19.5 MB (19462442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bc0431536f0b89ee088a790995dd293ec25d3688eb9ca73359b82336dd8768`  
		Last Modified: Thu, 16 Mar 2023 02:57:05 GMT  
		Size: 44.5 MB (44529856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbabb516d40e0733a3335db3a801c1d210be0e2c9afd8adfd32db5c4cd9d518c`  
		Last Modified: Thu, 16 Mar 2023 02:56:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162837bfbbd64039ee4257e98c01d2ee735e529ba6c3db116879af03d10394ff`  
		Last Modified: Thu, 16 Mar 2023 04:47:30 GMT  
		Size: 233.2 MB (233220701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3741ea3b9c8f232fc4341c907a62fd01ffbdb1aa6d876d0cd2b00952d9dc4f27`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 4.2 KB (4224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d674ecb316d5958afe3ed25d77276f9b318841fa534a99bc3f07a4458004b`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79817a7b907cfac994784d46ffb2efba1ca1bbde59ab25736bf121ff6cf7d16`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 8.1 KB (8088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cd4541998525c86de76ce4b4e78a588dbcaba6f0de0c85d2ab715c6cc2250e`  
		Last Modified: Thu, 16 Mar 2023 04:47:18 GMT  
		Size: 1.4 MB (1394644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1.1` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:5fb2c69ebadcdc76017fc3a76326d24b45e0e57bcc239fc3a1c88f37f2206618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329617407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a621b7f499b8a7e163383c98308d68a3ca9118674c4ff5be9134373854336693`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:51:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:54:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:54:31 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:55:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:55:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:52 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 06:14:54 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 06:14:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 06:14:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 06:14:56 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 06:15:03 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 06:15:03 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 06:15:03 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 06:15:03 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 06:15:03 GMT
USER 8983
# Thu, 16 Mar 2023 06:15:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:15:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f091a26bf16cf9bb9b5741a2f8b70047ee293b3a06b86283bea82ea46a9343a2`  
		Last Modified: Thu, 16 Mar 2023 02:00:21 GMT  
		Size: 20.8 MB (20810964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b693cb82e58b3095ebe84d13ae1a3782dd356f500a91d5a61a47e8235d6e2a67`  
		Last Modified: Thu, 16 Mar 2023 02:01:11 GMT  
		Size: 46.4 MB (46422408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d34498a6f57f8c837ca795570cb62efb66090dab255070ba11325965a0200`  
		Last Modified: Thu, 16 Mar 2023 02:01:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0484642c6ee51824c667f3e27f52270960e3c92c69bc7bfa7ab2f782763fddbd`  
		Last Modified: Thu, 16 Mar 2023 06:17:19 GMT  
		Size: 233.7 MB (233731740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d5eb156f2c791d6c94fa684d3c306e30c0060b7092c019d543a6d1852a61ea`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 4.3 KB (4328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e44d81a875819e3b33e6276257dfa34ff3fee5f4902c09c68a9a3947261064`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af30bf8591fec4083df823499a619bb2721cd6706e16b24f875198b29d551d3`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 8.1 KB (8086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab9e27d15fb1977ad5d628a5a3a00c2e7654d73d672edcd6fab2e1f282fe9c3`  
		Last Modified: Thu, 16 Mar 2023 06:17:11 GMT  
		Size: 1.4 MB (1443341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1.1` - linux; ppc64le

```console
$ docker pull solr@sha256:a1a69fd4bbdce4625f7837b11b1952be0acc8ad0e5691b614cdfdf382825a79c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338360960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273cc069c12a97e236bf1acf088a6f61503a29182993e85dc6a2112857da0650`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:03:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:09:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:09:28 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:11:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:11:43 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 07:57:46 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 02 Mar 2023 07:57:46 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 02 Mar 2023 07:57:46 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 02 Mar 2023 07:57:47 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 07:57:47 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 07:57:48 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 07:57:49 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 07:57:49 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 07:58:46 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 07:58:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 07:58:51 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 07:58:52 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 07:58:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 07:58:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 07:58:55 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 07:58:56 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 02 Mar 2023 07:58:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 07:58:57 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 07:58:58 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 07:59:00 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 07:59:02 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 07:59:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 07:59:17 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 07:59:18 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 07:59:19 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 07:59:20 GMT
USER 8983
# Thu, 02 Mar 2023 07:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:59:21 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcfd4c29e2858c629cdac7eee60bc7ba8dbd107ea7da4bb03b547506c38308e`  
		Last Modified: Thu, 02 Mar 2023 04:21:16 GMT  
		Size: 22.1 MB (22061782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb82256c20da7e07eaa4b9538f7c2b25e0823298b196b10b8d4cc0b99bb0b94`  
		Last Modified: Thu, 02 Mar 2023 04:22:44 GMT  
		Size: 46.8 MB (46780912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3ce9b4e4142f138693e5dd2bd9a282c82a6963375ebe137fba2ed271e46671`  
		Last Modified: Thu, 02 Mar 2023 04:22:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d986be7d3c9ab324621927aec65f9fdfa3b082f68680d6c6e406bd7328ead5f`  
		Last Modified: Thu, 02 Mar 2023 08:03:53 GMT  
		Size: 234.6 MB (234601089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347ffb373d6504149a76986fd243e6988db6deddde6ebaa33c51549a38eb6cf2`  
		Last Modified: Thu, 02 Mar 2023 08:03:33 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975892b8586cde02378134e1e956ba93deb4a0b519be943ccf87ef443e1b70af`  
		Last Modified: Thu, 02 Mar 2023 08:03:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5d01fecfd669830cd0ac0beb0d2f5fe801f8abb743ec2180ab287f69881060`  
		Last Modified: Thu, 02 Mar 2023 08:03:33 GMT  
		Size: 8.1 KB (8092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d4ab2e2e721ee0101a12b9a3c535eb75392c6c1a2c3ef78140cd647e82870`  
		Last Modified: Thu, 02 Mar 2023 08:03:34 GMT  
		Size: 1.6 MB (1604030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9.1.1` - linux; s390x

```console
$ docker pull solr@sha256:eff2d2656441173f360d5e3634c57ff9f29f53d4b1324f923c0dc67fef5f4dc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325448846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39edd1c02dba77220e37814fd47d672811b28086a85635337f4f20f5d98c9aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 02:28:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:28:26 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 02:29:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 02:29:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 19:30:19 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 02 Mar 2023 19:30:19 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 02 Mar 2023 19:30:19 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 02 Mar 2023 19:30:20 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 19:30:21 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 19:30:21 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 19:30:21 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 19:30:22 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 19:31:02 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 19:31:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 19:31:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 19:31:17 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 19:31:17 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 19:31:17 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 19:31:18 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 19:31:19 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 02 Mar 2023 19:31:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 19:31:19 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 19:31:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 19:31:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 19:31:23 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 19:31:29 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 19:31:29 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 19:31:29 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 19:31:30 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 19:31:30 GMT
USER 8983
# Thu, 02 Mar 2023 19:31:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:31:30 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d6ac74ab42247b9491b6986614b9868ce755dc1c84611543400690873aa73416`  
		Last Modified: Thu, 02 Mar 2023 02:22:20 GMT  
		Size: 27.0 MB (27016384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c998886554c68bd1179c9b0681699894e6a218a2f8938bc21ff5946911711b9f`  
		Last Modified: Thu, 02 Mar 2023 02:34:49 GMT  
		Size: 19.5 MB (19526654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70257de6ab5ab2c547fb3a6f33eed2a87916d198595947517941463e6375c4de`  
		Last Modified: Thu, 02 Mar 2023 02:35:32 GMT  
		Size: 43.7 MB (43739796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f11339ff9a469ece5c3c80559c9a7e5a683363b6831a2c472000f08938f0a`  
		Last Modified: Thu, 02 Mar 2023 02:35:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2711b71f04831e4899a5ad0c74d93214103e744afbba172e243f1751ec69fe`  
		Last Modified: Thu, 02 Mar 2023 19:35:01 GMT  
		Size: 233.7 MB (233657272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c59a45b188ab6ea12f698f22a2607d81439f247fbf86f11a7317dbfb959d29f`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20fb411eb8f75d9bf9d9085bb56ad644952e6bc9abd1fb4bc5fd32f226e8013`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfa5bf288d7135799a3012bd7a3d2a1d04174e5df83756460e4d996bb74b583`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 8.1 KB (8083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f841e66895f7471899ddcc0d3eee90def05320cbd1311576e68c6a11fa97eb7e`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 1.5 MB (1495950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `solr:latest`

```console
$ docker pull solr@sha256:83e18655f0f423379c2607cbad94fda486b1b3dcad6066defca8c18d6cdf75b3
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
$ docker pull solr@sha256:7ae731cf7ade88408e539274648e4bf7b30ea10d54369bf0615b5bb5389e96db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330942272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb94e6b98a98caf4732577e39d235cc284e6e40db07df661911b79a24d931760`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 04:53:01 GMT
ARG RELEASE
# Wed, 01 Mar 2023 04:53:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 04:53:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 04:53:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 04:53:03 GMT
ADD file:3478fb5bdcf8ad03d450d48901a6a8452c0ab253f24d21b1e27f99259db2d26b in / 
# Wed, 01 Mar 2023 04:53:04 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:03:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:04:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:04:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 10:03:53 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 10:03:54 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 10:03:54 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 10:03:54 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 10:04:19 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 10:04:20 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 02 Mar 2023 10:04:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 10:04:21 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 10:04:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 10:04:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 10:04:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 10:04:31 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 10:04:31 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 10:04:31 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 10:04:31 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 10:04:31 GMT
USER 8983
# Thu, 02 Mar 2023 10:04:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:04:31 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:df6635ed1257a768a4cf0fba31ebc5c8a6a03ae7d5b9b079bfd9df9eb89e0f81`  
		Last Modified: Wed, 01 Mar 2023 09:05:18 GMT  
		Size: 28.6 MB (28578002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedde91f7fda56da911564f824cff490cec019cf9146119947787937b628e7e9`  
		Last Modified: Thu, 02 Mar 2023 04:10:16 GMT  
		Size: 20.1 MB (20091922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d255ae1b0e629f899b27cf436e936ab95457801ac0a81a67d69463b74cd06ec2`  
		Last Modified: Thu, 02 Mar 2023 04:11:18 GMT  
		Size: 46.9 MB (46936990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af911ce721372f9284a012407b5c6205e056dc377a5c4457069b43207ffa6d8`  
		Last Modified: Thu, 02 Mar 2023 04:11:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a4a05be9271679d4b2d626e8e7bd946145213ce56b5b36ffa6b4a8bf9ca8ec`  
		Last Modified: Thu, 02 Mar 2023 10:24:07 GMT  
		Size: 233.7 MB (233741006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8596a8fd15162ffe7b169c0904392684c3728c7039c1e716c64b1cef496c483`  
		Last Modified: Thu, 02 Mar 2023 10:23:56 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1445a693048ede3241afc393c9796f6811abfbd63ad734c9fb558d41d55bf5`  
		Last Modified: Thu, 02 Mar 2023 10:23:56 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fafdf0f6dacb75209cc6ddf890dd7ac9742fe16e8b42deb0d87e9e15fb4d63`  
		Last Modified: Thu, 02 Mar 2023 10:23:56 GMT  
		Size: 8.1 KB (8083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f442192fc13ee950d548797565452341f99ab8825e2b303620561dddc0c646db`  
		Last Modified: Thu, 02 Mar 2023 10:23:57 GMT  
		Size: 1.6 MB (1581596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; arm variant v7

```console
$ docker pull solr@sha256:87c2c91166b2effd7b5c252d06181f1e89874156003048505800ab3f26dce775
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323206815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5157911afde46379c02997af2aa4fac83892ab68a6bfed5e0779f98fca7591`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:45:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:48:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:48:47 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:50:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:50:01 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:44:24 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 16 Mar 2023 04:44:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 04:44:26 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 04:44:26 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 04:44:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 04:44:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 04:44:36 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 04:44:36 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 04:44:36 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 04:44:36 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 04:44:36 GMT
USER 8983
# Thu, 16 Mar 2023 04:44:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 04:44:36 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1244137e4b88ca1866cf46370a384651ad01ecf13089022ced8c41a497b37663`  
		Last Modified: Thu, 16 Mar 2023 02:55:57 GMT  
		Size: 19.5 MB (19462442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bc0431536f0b89ee088a790995dd293ec25d3688eb9ca73359b82336dd8768`  
		Last Modified: Thu, 16 Mar 2023 02:57:05 GMT  
		Size: 44.5 MB (44529856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbabb516d40e0733a3335db3a801c1d210be0e2c9afd8adfd32db5c4cd9d518c`  
		Last Modified: Thu, 16 Mar 2023 02:56:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162837bfbbd64039ee4257e98c01d2ee735e529ba6c3db116879af03d10394ff`  
		Last Modified: Thu, 16 Mar 2023 04:47:30 GMT  
		Size: 233.2 MB (233220701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3741ea3b9c8f232fc4341c907a62fd01ffbdb1aa6d876d0cd2b00952d9dc4f27`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 4.2 KB (4224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d674ecb316d5958afe3ed25d77276f9b318841fa534a99bc3f07a4458004b`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79817a7b907cfac994784d46ffb2efba1ca1bbde59ab25736bf121ff6cf7d16`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 8.1 KB (8088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cd4541998525c86de76ce4b4e78a588dbcaba6f0de0c85d2ab715c6cc2250e`  
		Last Modified: Thu, 16 Mar 2023 04:47:18 GMT  
		Size: 1.4 MB (1394644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:5fb2c69ebadcdc76017fc3a76326d24b45e0e57bcc239fc3a1c88f37f2206618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329617407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a621b7f499b8a7e163383c98308d68a3ca9118674c4ff5be9134373854336693`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:51:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:54:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:54:31 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:55:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:55:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:52 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 06:14:54 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 06:14:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 06:14:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 06:14:56 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 06:15:03 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 06:15:03 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 06:15:03 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 06:15:03 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 06:15:03 GMT
USER 8983
# Thu, 16 Mar 2023 06:15:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:15:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f091a26bf16cf9bb9b5741a2f8b70047ee293b3a06b86283bea82ea46a9343a2`  
		Last Modified: Thu, 16 Mar 2023 02:00:21 GMT  
		Size: 20.8 MB (20810964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b693cb82e58b3095ebe84d13ae1a3782dd356f500a91d5a61a47e8235d6e2a67`  
		Last Modified: Thu, 16 Mar 2023 02:01:11 GMT  
		Size: 46.4 MB (46422408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d34498a6f57f8c837ca795570cb62efb66090dab255070ba11325965a0200`  
		Last Modified: Thu, 16 Mar 2023 02:01:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0484642c6ee51824c667f3e27f52270960e3c92c69bc7bfa7ab2f782763fddbd`  
		Last Modified: Thu, 16 Mar 2023 06:17:19 GMT  
		Size: 233.7 MB (233731740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d5eb156f2c791d6c94fa684d3c306e30c0060b7092c019d543a6d1852a61ea`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 4.3 KB (4328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e44d81a875819e3b33e6276257dfa34ff3fee5f4902c09c68a9a3947261064`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af30bf8591fec4083df823499a619bb2721cd6706e16b24f875198b29d551d3`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 8.1 KB (8086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab9e27d15fb1977ad5d628a5a3a00c2e7654d73d672edcd6fab2e1f282fe9c3`  
		Last Modified: Thu, 16 Mar 2023 06:17:11 GMT  
		Size: 1.4 MB (1443341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:a1a69fd4bbdce4625f7837b11b1952be0acc8ad0e5691b614cdfdf382825a79c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338360960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273cc069c12a97e236bf1acf088a6f61503a29182993e85dc6a2112857da0650`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:25:21 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:25:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:25:22 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:25:25 GMT
ADD file:8ec53343ee3a54689d663a250c785fbf7b8ac0c74de561582d2e54878e2d73b5 in / 
# Wed, 01 Mar 2023 05:25:25 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 04:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 04:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:03:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 04:09:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:09:28 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 04:11:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 04:11:43 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 07:57:46 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 02 Mar 2023 07:57:46 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 02 Mar 2023 07:57:46 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 02 Mar 2023 07:57:47 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 07:57:47 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 07:57:48 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 07:57:49 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 07:57:49 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 07:58:46 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 07:58:50 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 07:58:51 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 07:58:52 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 07:58:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 07:58:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 07:58:55 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 07:58:56 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 02 Mar 2023 07:58:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 07:58:57 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 07:58:58 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 07:59:00 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 07:59:02 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 07:59:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 07:59:17 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 07:59:18 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 07:59:19 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 07:59:20 GMT
USER 8983
# Thu, 02 Mar 2023 07:59:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:59:21 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:4ecbbabc4a8d11d32aa94bd1d645cba73ad91f59060b872eaf684de51310281b`  
		Last Modified: Thu, 02 Mar 2023 03:56:04 GMT  
		Size: 33.3 MB (33300379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcfd4c29e2858c629cdac7eee60bc7ba8dbd107ea7da4bb03b547506c38308e`  
		Last Modified: Thu, 02 Mar 2023 04:21:16 GMT  
		Size: 22.1 MB (22061782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb82256c20da7e07eaa4b9538f7c2b25e0823298b196b10b8d4cc0b99bb0b94`  
		Last Modified: Thu, 02 Mar 2023 04:22:44 GMT  
		Size: 46.8 MB (46780912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3ce9b4e4142f138693e5dd2bd9a282c82a6963375ebe137fba2ed271e46671`  
		Last Modified: Thu, 02 Mar 2023 04:22:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d986be7d3c9ab324621927aec65f9fdfa3b082f68680d6c6e406bd7328ead5f`  
		Last Modified: Thu, 02 Mar 2023 08:03:53 GMT  
		Size: 234.6 MB (234601089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347ffb373d6504149a76986fd243e6988db6deddde6ebaa33c51549a38eb6cf2`  
		Last Modified: Thu, 02 Mar 2023 08:03:33 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975892b8586cde02378134e1e956ba93deb4a0b519be943ccf87ef443e1b70af`  
		Last Modified: Thu, 02 Mar 2023 08:03:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5d01fecfd669830cd0ac0beb0d2f5fe801f8abb743ec2180ab287f69881060`  
		Last Modified: Thu, 02 Mar 2023 08:03:33 GMT  
		Size: 8.1 KB (8092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d4ab2e2e721ee0101a12b9a3c535eb75392c6c1a2c3ef78140cd647e82870`  
		Last Modified: Thu, 02 Mar 2023 08:03:34 GMT  
		Size: 1.6 MB (1604030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:eff2d2656441173f360d5e3634c57ff9f29f53d4b1324f923c0dc67fef5f4dc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325448846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39edd1c02dba77220e37814fd47d672811b28086a85635337f4f20f5d98c9aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 01 Mar 2023 05:41:15 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:41:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:41:15 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:41:17 GMT
ADD file:859bfd657725af24f17d4e3c5b3b583b4b29d55f5f7f2f44fbdd6fbc83c6952d in / 
# Wed, 01 Mar 2023 05:41:17 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:26:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 02 Mar 2023 02:28:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:28:26 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 02 Mar 2023 02:29:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 02 Mar 2023 02:29:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 02 Mar 2023 19:30:19 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 02 Mar 2023 19:30:19 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 02 Mar 2023 19:30:19 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 02 Mar 2023 19:30:20 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 02 Mar 2023 19:30:21 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 02 Mar 2023 19:30:21 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 19:30:21 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 19:30:22 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 02 Mar 2023 19:31:02 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 02 Mar 2023 19:31:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 02 Mar 2023 19:31:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 02 Mar 2023 19:31:17 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 02 Mar 2023 19:31:17 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 02 Mar 2023 19:31:17 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 02 Mar 2023 19:31:18 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 02 Mar 2023 19:31:19 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 02 Mar 2023 19:31:19 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 02 Mar 2023 19:31:19 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 02 Mar 2023 19:31:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 02 Mar 2023 19:31:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 02 Mar 2023 19:31:23 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 02 Mar 2023 19:31:29 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 02 Mar 2023 19:31:29 GMT
VOLUME [/var/solr]
# Thu, 02 Mar 2023 19:31:29 GMT
EXPOSE 8983
# Thu, 02 Mar 2023 19:31:30 GMT
WORKDIR /opt/solr
# Thu, 02 Mar 2023 19:31:30 GMT
USER 8983
# Thu, 02 Mar 2023 19:31:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Mar 2023 19:31:30 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:d6ac74ab42247b9491b6986614b9868ce755dc1c84611543400690873aa73416`  
		Last Modified: Thu, 02 Mar 2023 02:22:20 GMT  
		Size: 27.0 MB (27016384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c998886554c68bd1179c9b0681699894e6a218a2f8938bc21ff5946911711b9f`  
		Last Modified: Thu, 02 Mar 2023 02:34:49 GMT  
		Size: 19.5 MB (19526654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70257de6ab5ab2c547fb3a6f33eed2a87916d198595947517941463e6375c4de`  
		Last Modified: Thu, 02 Mar 2023 02:35:32 GMT  
		Size: 43.7 MB (43739796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916f11339ff9a469ece5c3c80559c9a7e5a683363b6831a2c472000f08938f0a`  
		Last Modified: Thu, 02 Mar 2023 02:35:26 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2711b71f04831e4899a5ad0c74d93214103e744afbba172e243f1751ec69fe`  
		Last Modified: Thu, 02 Mar 2023 19:35:01 GMT  
		Size: 233.7 MB (233657272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c59a45b188ab6ea12f698f22a2607d81439f247fbf86f11a7317dbfb959d29f`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20fb411eb8f75d9bf9d9085bb56ad644952e6bc9abd1fb4bc5fd32f226e8013`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfa5bf288d7135799a3012bd7a3d2a1d04174e5df83756460e4d996bb74b583`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 8.1 KB (8083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f841e66895f7471899ddcc0d3eee90def05320cbd1311576e68c6a11fa97eb7e`  
		Last Modified: Thu, 02 Mar 2023 19:34:50 GMT  
		Size: 1.5 MB (1495950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
