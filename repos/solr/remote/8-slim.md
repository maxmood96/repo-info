## `solr:8-slim`

```console
$ docker pull solr@sha256:eb249e6b4b88b35dc903a0ff124fb420553615b6d0a08df165fec6ac49998785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `solr:8-slim` - linux; amd64

```console
$ docker pull solr@sha256:d6027fdbb823cf5a06046efd5a7745f4e14e0c2fd8cce4596182088608df72e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290070204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e384608b110098f2a066fcefd467a2d65a208086b65db5e7bd2b784878fd84ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:40 GMT
ADD file:5e8343ab9a73edc27c2889634896e792ab289b85c206de0fc31183fdc0a32ac7 in / 
# Tue, 17 Aug 2021 01:23:41 GMT
CMD ["bash"]
# Thu, 26 Aug 2021 00:33:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 26 Aug 2021 00:36:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 26 Aug 2021 00:36:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 26 Aug 2021 00:36:15 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Aug 2021 00:36:15 GMT
ENV LANG=C.UTF-8
# Thu, 26 Aug 2021 00:36:15 GMT
ENV JAVA_VERSION=11.0.12
# Thu, 26 Aug 2021 00:37:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Thu, 26 Aug 2021 03:22:21 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 26 Aug 2021 03:22:21 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 26 Aug 2021 03:22:21 GMT
ARG SOLR_VERSION=8.9.0
# Thu, 26 Aug 2021 03:22:21 GMT
ARG SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242
# Thu, 26 Aug 2021 03:22:21 GMT
ARG SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969
# Thu, 26 Aug 2021 03:22:22 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 26 Aug 2021 03:22:22 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 26 Aug 2021 03:22:29 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 26 Aug 2021 03:22:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.9.0/solr-8.9.0.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.9.0/solr-8.9.0.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.9.0/solr-8.9.0.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 26 Aug 2021 03:22:30 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 26 Aug 2021 03:22:32 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 26 Aug 2021 03:22:40 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 26 Aug 2021 03:22:40 GMT
COPY --chown=0:0dir:9bc5f3733a819401f8f06067a2f41713605d2c3bb03bbbe92d04dc2f83bd0265 in /opt/docker-solr/scripts 
# Thu, 26 Aug 2021 03:22:41 GMT
VOLUME [/var/solr]
# Thu, 26 Aug 2021 03:22:41 GMT
EXPOSE 8983
# Thu, 26 Aug 2021 03:22:41 GMT
WORKDIR /opt/solr
# Thu, 26 Aug 2021 03:22:41 GMT
USER solr
# Thu, 26 Aug 2021 03:22:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Aug 2021 03:22:42 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:99046ad9247f8a1cbd1048d9099d026191ad9cda63c08aadeb704b7000a51717`  
		Last Modified: Tue, 17 Aug 2021 01:29:35 GMT  
		Size: 31.4 MB (31361314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97c10298fea9915576e7ff72c6eca3d7c589aaafd6bc6481a5814c4271d2251`  
		Last Modified: Thu, 26 Aug 2021 00:43:26 GMT  
		Size: 1.6 MB (1581998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad67722a7508cc8ca694c9e75efebc7c37f65d179dc2d6f36a9a1615dc5206c`  
		Last Modified: Thu, 26 Aug 2021 00:48:02 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbeb29d69a7c2580a75906597d7cd4d59a9eff12b482810794fa01b105155358`  
		Last Modified: Thu, 26 Aug 2021 00:49:22 GMT  
		Size: 47.1 MB (47126663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552d3b6e26040a46f662414654918d023856981ca307451a46beff186807308b`  
		Last Modified: Thu, 26 Aug 2021 03:42:12 GMT  
		Size: 6.9 MB (6898017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87200e6e526a64f2e7e09a20dfc13da5cd9b8d73eb3b8e8e6fdd11de4fc63729`  
		Last Modified: Thu, 26 Aug 2021 03:42:11 GMT  
		Size: 4.3 KB (4289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f428b2eb3fd584bdfb8df916f023757e838b07f48ea7810e80005ae161a018c1`  
		Last Modified: Thu, 26 Aug 2021 03:42:11 GMT  
		Size: 2.9 KB (2925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c100b17608b7352339b14453d042ec36c52f109e1129ad944e5a7801cb53401f`  
		Last Modified: Thu, 26 Aug 2021 03:42:21 GMT  
		Size: 203.1 MB (203088512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7021ca775a54e2d52e3315bd204d05c76411ef47b31c74441b567f421a03b9a7`  
		Last Modified: Thu, 26 Aug 2021 03:42:11 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:d60f23ca993d2f74c2ba68b9ecd69681126c91aa8ac4fcc8704dc8d26b03c0c5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287737769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd02550f14e79b7b4ac4a869a9cfaf4c7975a5352fc2324fff864a77aa9858b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 03 Sep 2021 00:40:33 GMT
ADD file:9600a4686ae105acffa54787a7c81f5252e90023cbcfbe37519150b954110c5c in / 
# Fri, 03 Sep 2021 00:40:34 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 10:44:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 10:49:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Fri, 03 Sep 2021 10:50:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Fri, 03 Sep 2021 10:50:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 10:50:00 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 10:50:00 GMT
ENV JAVA_VERSION=11.0.12
# Fri, 03 Sep 2021 10:52:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 04 Sep 2021 02:52:37 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Sat, 04 Sep 2021 02:52:37 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Sat, 04 Sep 2021 02:52:37 GMT
ARG SOLR_VERSION=8.9.0
# Sat, 04 Sep 2021 02:52:37 GMT
ARG SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242
# Sat, 04 Sep 2021 02:52:38 GMT
ARG SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969
# Sat, 04 Sep 2021 02:52:38 GMT
ARG SOLR_DOWNLOAD_URL
# Sat, 04 Sep 2021 02:52:38 GMT
ARG SOLR_DOWNLOAD_SERVER
# Sat, 04 Sep 2021 02:52:45 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Sat, 04 Sep 2021 02:52:45 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.9.0/solr-8.9.0.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.9.0/solr-8.9.0.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.9.0/solr-8.9.0.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Sat, 04 Sep 2021 02:52:46 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Sat, 04 Sep 2021 02:52:53 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Sat, 04 Sep 2021 02:53:01 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Sat, 04 Sep 2021 02:53:01 GMT
COPY --chown=0:0dir:9bc5f3733a819401f8f06067a2f41713605d2c3bb03bbbe92d04dc2f83bd0265 in /opt/docker-solr/scripts 
# Sat, 04 Sep 2021 02:53:01 GMT
VOLUME [/var/solr]
# Sat, 04 Sep 2021 02:53:02 GMT
EXPOSE 8983
# Sat, 04 Sep 2021 02:53:02 GMT
WORKDIR /opt/solr
# Sat, 04 Sep 2021 02:53:02 GMT
USER solr
# Sat, 04 Sep 2021 02:53:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Sep 2021 02:53:02 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:1901ca797b5ea06f6a4facc81ad772177fdd833ed4329dc86ef126078633b949`  
		Last Modified: Fri, 03 Sep 2021 00:48:51 GMT  
		Size: 30.1 MB (30055483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cacb51d4ac932821c4ef93d9b1b99d91b46e6936de614b998343b89d39ca977`  
		Last Modified: Fri, 03 Sep 2021 11:04:46 GMT  
		Size: 1.6 MB (1566199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e9f812da0080ddec70341131e623a671f11e1a8990c61ce534bed5bb272081`  
		Last Modified: Fri, 03 Sep 2021 11:14:24 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca49002e50182441d3138e87c0aad5647fbe301fc8ed5fb106c9e5a56e3ea0f2`  
		Last Modified: Fri, 03 Sep 2021 11:17:23 GMT  
		Size: 46.2 MB (46200075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adc763bfa4c39539ccfff450419fc99863d6c1c42e7a9e55a71c1f01018aa4a`  
		Last Modified: Sat, 04 Sep 2021 03:10:28 GMT  
		Size: 6.8 MB (6813798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb12a41b7e2a52845bd64947dedfa7c06b1e82eb2d1614103664160ba6ca5a4b`  
		Last Modified: Sat, 04 Sep 2021 03:10:26 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05321dee111133ddd9733d32e2d5f773c5d5cd3226a121466b798a11142663aa`  
		Last Modified: Sat, 04 Sep 2021 03:10:27 GMT  
		Size: 2.9 KB (2931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5ad071ff4f9d4e09715f08ea7a1f6cd20451107416b58ae741d0602ed96d59`  
		Last Modified: Sat, 04 Sep 2021 03:10:40 GMT  
		Size: 203.1 MB (203088481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f726c6d7c156490d3005cc4d5ddb97e2d624fbbe9fee863960b653e9e7c056d`  
		Last Modified: Sat, 04 Sep 2021 03:10:26 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
