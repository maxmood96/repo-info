## `solr:8-slim`

```console
$ docker pull solr@sha256:ae46d6e1a09c72d0b86f417e290b3f82155ca368d2f83682bdae086a3005cb5f
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
$ docker pull solr@sha256:c261d7a246b9cb612c26292bdad3b22a18aeca46a76b409ea535e62c067cf382
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315608847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d243c80f97317cbd983eefdda93ae500f0b2a2bdd71f120ee17f0c2e02b0c7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 02:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 02:34:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:20:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:22:00 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Tue, 08 Aug 2023 19:22:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:22:46 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 08 Aug 2023 19:22:46 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 19:22:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 20:32:16 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 08 Aug 2023 20:32:16 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 08 Aug 2023 20:32:17 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 08 Aug 2023 20:32:17 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 08 Aug 2023 20:32:17 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 08 Aug 2023 20:32:17 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 08 Aug 2023 20:32:17 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 08 Aug 2023 20:32:24 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 08 Aug 2023 20:32:24 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 08 Aug 2023 20:32:24 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 08 Aug 2023 20:32:33 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 08 Aug 2023 20:33:05 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 08 Aug 2023 20:33:06 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 08 Aug 2023 20:33:06 GMT
VOLUME [/var/solr]
# Tue, 08 Aug 2023 20:33:06 GMT
EXPOSE 8983
# Tue, 08 Aug 2023 20:33:06 GMT
WORKDIR /opt/solr
# Tue, 08 Aug 2023 20:33:06 GMT
USER 8983
# Tue, 08 Aug 2023 20:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 20:33:06 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f32e041863d53bbb7f9f65ba31f023a9f344dd4105bf5345c6e748e3cc3e71a`  
		Last Modified: Tue, 08 Aug 2023 19:26:48 GMT  
		Size: 16.9 MB (16919807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74b53e563fbe286fa6ea6f80b4807766d6c850cff6be0125187fd11534f3582`  
		Last Modified: Tue, 08 Aug 2023 19:30:36 GMT  
		Size: 46.9 MB (46863049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7aefa3f03a208ec5e8794db4087a1d0143303e020fba42db8efd12079becf2e`  
		Last Modified: Tue, 08 Aug 2023 19:30:30 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41de81daf06b94a19ef6f3ff861abcdd0346427dd1863dbdc5f48ea6a949ce73`  
		Last Modified: Tue, 08 Aug 2023 19:30:30 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e58e3fe486494a0deb95e98cae4a349a19d4e81e50255a208d03eb2095e645c`  
		Last Modified: Tue, 08 Aug 2023 20:35:30 GMT  
		Size: 4.9 MB (4902167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ccc9c472d4f066655aae2da0f4a105a8f1ef6081e1871cc42ace3eb443548a`  
		Last Modified: Tue, 08 Aug 2023 20:35:29 GMT  
		Size: 4.3 KB (4293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dbe90600912c649ab0732766f76c975bc82aac4da820bc7e8923b568552d7e`  
		Last Modified: Tue, 08 Aug 2023 20:35:29 GMT  
		Size: 3.5 KB (3471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c9fbcdb242fb67da4cbbff8d73b021ee3a8e017ef84f44054c0f60c74906db`  
		Last Modified: Tue, 08 Aug 2023 20:35:43 GMT  
		Size: 218.3 MB (218328256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7306e12d0ff7c3a281b19b5d12588fba24c209a3eb803dbcc795e73cc67d34f2`  
		Last Modified: Tue, 08 Aug 2023 20:35:29 GMT  
		Size: 6.3 KB (6308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:fdf8ae681350f83d697d6e2f4f7dbae0bb60b1ec8994b453b0256cb49dbb8c43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307805336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d54af1d1d90c08494ce288f89f928689770097770ed43a849f300525548729`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:45 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:49 GMT
ADD file:60aa8465a6ba5538decc41365cc9b78ae86131e8c2cfc9177b4a336354ead988 in / 
# Tue, 01 Aug 2023 06:16:50 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:27:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 01:27:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 01:27:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 18:57:54 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 18:59:47 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Tue, 08 Aug 2023 19:00:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:00:26 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Mon, 14 Aug 2023 18:09:45 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:09:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Aug 2023 19:19:37 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Mon, 14 Aug 2023 19:19:37 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Mon, 14 Aug 2023 19:19:37 GMT
ARG SOLR_VERSION=8.11.2
# Mon, 14 Aug 2023 19:19:37 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Mon, 14 Aug 2023 19:19:37 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Mon, 14 Aug 2023 19:19:37 GMT
ARG SOLR_DOWNLOAD_URL
# Mon, 14 Aug 2023 19:19:37 GMT
ARG SOLR_DOWNLOAD_SERVER
# Mon, 14 Aug 2023 19:19:43 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Mon, 14 Aug 2023 19:19:43 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Mon, 14 Aug 2023 19:19:44 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Mon, 14 Aug 2023 19:19:53 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Mon, 14 Aug 2023 19:20:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Mon, 14 Aug 2023 19:20:30 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Mon, 14 Aug 2023 19:20:30 GMT
VOLUME [/var/solr]
# Mon, 14 Aug 2023 19:20:30 GMT
EXPOSE 8983
# Mon, 14 Aug 2023 19:20:30 GMT
WORKDIR /opt/solr
# Mon, 14 Aug 2023 19:20:30 GMT
USER 8983
# Mon, 14 Aug 2023 19:20:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Aug 2023 19:20:30 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:c429b4536d4b2ab209b0a779f71ba68570f10acf9dd806c7e2011fce49bd5c97`  
		Last Modified: Wed, 02 Aug 2023 04:28:29 GMT  
		Size: 24.6 MB (24591882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cd3a8f320fb2da0d9f7694604e369817023cd4b7b62173714bbff7cad25aae`  
		Last Modified: Tue, 08 Aug 2023 19:02:31 GMT  
		Size: 15.7 MB (15659457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0093c473b1e40e62fd206d1bcc43b34fda02661fab4df01550be92363fc4e61`  
		Last Modified: Tue, 08 Aug 2023 19:04:38 GMT  
		Size: 45.0 MB (45013323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817239aeee7f7e1a21412276af40721187ad513f91fb0d6201ff50ca317dbc8d`  
		Last Modified: Tue, 08 Aug 2023 19:04:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4734b31a412e0129cd7e01eb19638b477abaec99dc44ae8c2041bdf6364d4d0c`  
		Last Modified: Mon, 14 Aug 2023 18:11:20 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489aa0aa1135c83077b19a61920b6dc5c3f60e7f8a3f79cfc117014d7e0ced02`  
		Last Modified: Mon, 14 Aug 2023 19:22:47 GMT  
		Size: 4.2 MB (4197557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef7325a156462fbc5800aeb2e3856ec9ee906f21c2543d618c05b700dc44dec`  
		Last Modified: Mon, 14 Aug 2023 19:22:46 GMT  
		Size: 4.2 KB (4223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae3bf552050db9453154adbeeae0c050bfeb99baba48e7fa6673b2b33776efd`  
		Last Modified: Mon, 14 Aug 2023 19:22:46 GMT  
		Size: 3.5 KB (3471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280743ac6e2d0fc579a6cbc6ce7c6e86d209fdf30ba68fb668b9e8d9f4ab5e06`  
		Last Modified: Mon, 14 Aug 2023 19:22:58 GMT  
		Size: 218.3 MB (218328225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dfb3376e96c7b75126deb6dac0fe5c190442ec9d794e82134e138da4f01118`  
		Last Modified: Mon, 14 Aug 2023 19:22:46 GMT  
		Size: 6.3 KB (6305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:b8e1683890678f1de192ba80f809df585a4be7709b12f13e1056707c4afc81a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312256285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9052422afc4672396210b5d8e30574c3268745d18bda64e9e29db3caf41504`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:05:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 01:05:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 01:05:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:40:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:41:09 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Tue, 08 Aug 2023 19:41:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:41:45 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 08 Aug 2023 19:41:45 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 19:41:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 21:42:23 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Tue, 08 Aug 2023 21:42:23 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Tue, 08 Aug 2023 21:42:23 GMT
ARG SOLR_VERSION=8.11.2
# Tue, 08 Aug 2023 21:42:23 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Tue, 08 Aug 2023 21:42:23 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Tue, 08 Aug 2023 21:42:24 GMT
ARG SOLR_DOWNLOAD_URL
# Tue, 08 Aug 2023 21:42:24 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 08 Aug 2023 21:42:29 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Tue, 08 Aug 2023 21:42:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Tue, 08 Aug 2023 21:42:30 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Tue, 08 Aug 2023 21:42:40 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Tue, 08 Aug 2023 21:43:12 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Tue, 08 Aug 2023 21:43:13 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Tue, 08 Aug 2023 21:43:13 GMT
VOLUME [/var/solr]
# Tue, 08 Aug 2023 21:43:13 GMT
EXPOSE 8983
# Tue, 08 Aug 2023 21:43:13 GMT
WORKDIR /opt/solr
# Tue, 08 Aug 2023 21:43:13 GMT
USER 8983
# Tue, 08 Aug 2023 21:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 21:43:14 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d3de389f9fd6a81c60e4d6444266df2002734ab5660161fa9bf374cd8cd473`  
		Last Modified: Tue, 08 Aug 2023 19:44:02 GMT  
		Size: 16.8 MB (16770361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30825ef4a91579dc8aea74f3af9c3ac54566d71a6a58e52508138dced7544e46`  
		Last Modified: Tue, 08 Aug 2023 19:46:45 GMT  
		Size: 45.2 MB (45190555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620827c69f936cc40faae455f389f19901c656949793c5279480e3e08b071868`  
		Last Modified: Tue, 08 Aug 2023 19:46:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7a5c7908fc95a0f78dab9acccfc13dc332ba447a48e739db1de06ed3117509`  
		Last Modified: Tue, 08 Aug 2023 19:46:39 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469dad6a467a6b676fd7f4194e8302bc582695e7c5fba789cf15e3d4f73210d3`  
		Last Modified: Tue, 08 Aug 2023 21:45:31 GMT  
		Size: 4.8 MB (4751645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9a5e705834d7969967d78ac7e393cb47ca9ddb4d04e7258966a5ef3175047a`  
		Last Modified: Tue, 08 Aug 2023 21:45:31 GMT  
		Size: 4.3 KB (4329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e9e8a2b084e4fd57eb07b9206ddd5f7e65750977b87b9b06b8e135c3b8e5aa`  
		Last Modified: Tue, 08 Aug 2023 21:45:31 GMT  
		Size: 3.5 KB (3472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266155a187124e7d6f11625ef2e95211c035901e68a3010210830b8e9f5bcfc8`  
		Last Modified: Tue, 08 Aug 2023 21:45:43 GMT  
		Size: 218.3 MB (218328201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645770be2335f84e25d477e8fc3d3d50bbfc5fb0182947f33339f45aca508cde`  
		Last Modified: Tue, 08 Aug 2023 21:45:31 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:8cf30da7975a470b335e59d48b90a4b4ba024f2285c60cd6ebb06d07e483af86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.9 MB (317939616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ac29a4fed9b9d3b6229e74ccbe2d660ffbf234a3196f8c6a0623f0c893aa7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:36 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:20:40 GMT
ADD file:822df76493d1d533c1a283ab7bb20ce81309f57279422a0eebb2ffb9fab55963 in / 
# Tue, 01 Aug 2023 06:20:40 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 02:44:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 02:44:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:18:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:20:50 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Tue, 08 Aug 2023 19:22:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:22:21 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Mon, 14 Aug 2023 18:09:52 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:09:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Aug 2023 18:59:11 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Mon, 14 Aug 2023 18:59:12 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Mon, 14 Aug 2023 18:59:12 GMT
ARG SOLR_VERSION=8.11.2
# Mon, 14 Aug 2023 18:59:13 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Mon, 14 Aug 2023 18:59:13 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Mon, 14 Aug 2023 18:59:14 GMT
ARG SOLR_DOWNLOAD_URL
# Mon, 14 Aug 2023 18:59:14 GMT
ARG SOLR_DOWNLOAD_SERVER
# Mon, 14 Aug 2023 18:59:34 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Mon, 14 Aug 2023 18:59:35 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Mon, 14 Aug 2023 18:59:37 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Mon, 14 Aug 2023 18:59:47 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Mon, 14 Aug 2023 19:00:19 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Mon, 14 Aug 2023 19:00:22 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Mon, 14 Aug 2023 19:00:22 GMT
VOLUME [/var/solr]
# Mon, 14 Aug 2023 19:00:22 GMT
EXPOSE 8983
# Mon, 14 Aug 2023 19:00:23 GMT
WORKDIR /opt/solr
# Mon, 14 Aug 2023 19:00:23 GMT
USER 8983
# Mon, 14 Aug 2023 19:00:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Aug 2023 19:00:24 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:be0253994e7bea97e6b44cdeec04bf996c8dd3380e70409de3783a1d1971e747`  
		Last Modified: Thu, 03 Aug 2023 02:50:24 GMT  
		Size: 33.3 MB (33306772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af03d96af036322b1cf090be8f29d0a3931c623558764bccaca2826ee7b9af6b`  
		Last Modified: Tue, 08 Aug 2023 19:28:27 GMT  
		Size: 18.2 MB (18215568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f16b42970b3a35a96a2c9932629f2542a785b3db4b590abf29c64fe6c16aa4`  
		Last Modified: Tue, 08 Aug 2023 19:32:47 GMT  
		Size: 42.3 MB (42295522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7e8fb6acda0c6ff08b9a9d42318ddf909f1dcef9e88b5c1a298d30b8999306`  
		Last Modified: Tue, 08 Aug 2023 19:32:36 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b99a0af9e9ba4b7b1cca950f0cc2819d6063ba606aa8d0cbce51181ed8da02`  
		Last Modified: Mon, 14 Aug 2023 18:11:52 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82d4efe17a1f7a7d189c1464f76fb3c610b60c12ecf59dc4c1786debd964b82`  
		Last Modified: Mon, 14 Aug 2023 19:04:22 GMT  
		Size: 5.8 MB (5778482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e326c4940e16b8d5db575e444b7dab57c2681ca561f0e9e2e1ab119240af26e`  
		Last Modified: Mon, 14 Aug 2023 19:04:20 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1141fab05c906a34a6a62164866f4e5cfe9e321e7505d351d1aca7dc0a5bdf`  
		Last Modified: Mon, 14 Aug 2023 19:04:20 GMT  
		Size: 3.5 KB (3470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b05c8a19a749006fe622d0f455fc093a11fc60e2ddfdbdc46f79e71caba63d`  
		Last Modified: Mon, 14 Aug 2023 19:04:40 GMT  
		Size: 218.3 MB (218328303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6befd4f667496fd052bb5329c62bdf342a2038fbce4a21145f855d48f2dbf1`  
		Last Modified: Mon, 14 Aug 2023 19:04:20 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; s390x

```console
$ docker pull solr@sha256:f61019de9c0cc601abe1c353e4367af7c64148835ef56a4e541566769ba02d1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307364409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2be3cd09c53ed33f96f048996e44e9651aac3707c0adbba19b0e95ddb6c371`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 01 Aug 2023 06:17:39 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:17:41 GMT
ADD file:36efc3ec29bb54e0987fe91be1aa7cc849909b3cd2534af3de2d3d07a03804cf in / 
# Tue, 01 Aug 2023 06:17:41 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 00:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 00:24:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 00:24:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:42:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:42:13 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Tue, 08 Aug 2023 19:43:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='45e190920fb3ec61ee5213a7bd98553abf2ae7692eb9daa504fcdc9d59a7cfc4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        armhf|arm)          ESUM='1e2a02364084b2d054e88a871f3efaa4450ae4f087b8f806fd95c15d5affcc7b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_arm_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='61034834b61bf080392218b25dcac2d9e3505b5e4f53539704d496be4181aadf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0c7050976914e0613179446de62bb20d2845ae809f6d31bc0ed8d136f8fd3d9b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ffb070c26ea22771f78769c569c9db3412e6486434dc6df1fd3c3438285766e7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 08 Aug 2023 19:43:25 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Mon, 14 Aug 2023 18:09:23 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:09:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Aug 2023 19:09:30 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Mon, 14 Aug 2023 19:09:30 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Mon, 14 Aug 2023 19:09:30 GMT
ARG SOLR_VERSION=8.11.2
# Mon, 14 Aug 2023 19:09:31 GMT
ARG SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa
# Mon, 14 Aug 2023 19:09:31 GMT
ARG SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E
# Mon, 14 Aug 2023 19:09:31 GMT
ARG SOLR_DOWNLOAD_URL
# Mon, 14 Aug 2023 19:09:31 GMT
ARG SOLR_DOWNLOAD_SERVER
# Mon, 14 Aug 2023 19:09:38 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v2.0/jattach; chmod 755 jattach;   echo >jattach.sha512 "a19e774600d6aa844bceb2189285848127a70130a69fb1840c10367f3360972c733b3f09e60e9672d387e2d48c750ab56acfe8f80f7c6af76f5d1123e5ad7222  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Mon, 14 Aug 2023 19:09:38 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.2/solr-8.11.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.2/solr-8.11.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Mon, 14 Aug 2023 19:09:39 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Mon, 14 Aug 2023 19:09:46 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Mon, 14 Aug 2023 19:10:18 GMT
# ARGS: SOLR_KEYS=86EDB9C33B8517228E88A8F93E48C0C6EF362B9E SOLR_SHA512=22fedcc0090eda72c3c5a5ea769c93adaf7d92c5c4479993f009ef0b9d42de5bd2ed1e0565ca01f3428587d8a3836286aa3017aab157050f2bd5bc3482fdebaa SOLR_VERSION=8.11.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Mon, 14 Aug 2023 19:10:27 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Mon, 14 Aug 2023 19:10:27 GMT
VOLUME [/var/solr]
# Mon, 14 Aug 2023 19:10:28 GMT
EXPOSE 8983
# Mon, 14 Aug 2023 19:10:28 GMT
WORKDIR /opt/solr
# Mon, 14 Aug 2023 19:10:28 GMT
USER 8983
# Mon, 14 Aug 2023 19:10:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Aug 2023 19:10:29 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:365fa2124eb5f6f369204f3fe0210d9965952628707dfacd4194a8e15caf0420`  
		Last Modified: Thu, 03 Aug 2023 00:03:37 GMT  
		Size: 27.0 MB (27014233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4bb71ff7cf2cdfba432549f8f118e2394ed9d63653317801c650fc5cdf556b`  
		Last Modified: Tue, 08 Aug 2023 19:46:12 GMT  
		Size: 16.6 MB (16643421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b7901e3458852aefab0cd7d218de7885480a6c539089b6d1bc425a7e6a489b`  
		Last Modified: Tue, 08 Aug 2023 19:46:59 GMT  
		Size: 40.6 MB (40631841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af005abe8cb8ae8675c28b7ac9276cc6cc1b953d703ad5cac418014baf282b49`  
		Last Modified: Tue, 08 Aug 2023 19:46:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb68cce6a6f20182e2900da727bcd44abc6cdf27d62759b828a75036b75ac9c`  
		Last Modified: Mon, 14 Aug 2023 18:11:24 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0922d53cda89b7f5fe5c81df02e4fed16ebf5a5d65d34a47e04725378e1a06`  
		Last Modified: Mon, 14 Aug 2023 19:12:46 GMT  
		Size: 4.7 MB (4731630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15da8707851fe55ef1b51eb90e38a0479d37b56528312afa8d65c3aac3257d4`  
		Last Modified: Mon, 14 Aug 2023 19:12:45 GMT  
		Size: 4.3 KB (4333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db45a0d4a42d119fbd1157d5cdbc36ad57c89e0ee89cdbf75debd24db241ba8`  
		Last Modified: Mon, 14 Aug 2023 19:12:45 GMT  
		Size: 3.5 KB (3476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16d867e5193dedab60a79f3aa3d893cc756e3340e05ae196af01d515102fb4be`  
		Last Modified: Mon, 14 Aug 2023 19:12:55 GMT  
		Size: 218.3 MB (218328273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be6ab3ffaa3640ef89674ce75f8ab2fb932200f538cdaa2880ae410f819c9df`  
		Last Modified: Mon, 14 Aug 2023 19:12:45 GMT  
		Size: 6.3 KB (6309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
