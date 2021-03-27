## `solr:latest`

```console
$ docker pull solr@sha256:d571eeb78006c402a02b2e958fa7a7c18683c4038ce8fbfbbe5794e90c5aecad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `solr:latest` - linux; amd64

```console
$ docker pull solr@sha256:bdf28127d52284ebbad68c7e5024c63d23a9dde39fb89e287d36dbfe6b926868
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.6 MB (319579457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b8bb9ef8cb44ead2d8bc0316b9c2d43644e1acdfc6b58ec8f9ea3bd1174be7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:41 GMT
ADD file:89234bb2f86c7eb890235a48904d1c9898a8d287a525c4fe5698d4a04cdd8f12 in / 
# Fri, 26 Mar 2021 15:20:42 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:53:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:53:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 12:54:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 12:54:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 27 Mar 2021 12:54:03 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 27 Mar 2021 12:54:03 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Mar 2021 12:54:03 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 12:54:03 GMT
ENV JAVA_VERSION=11.0.10
# Sat, 27 Mar 2021 12:54:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_x64_linux_11.0.10_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_aarch64_linux_11.0.10_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 27 Mar 2021 13:31:43 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Sat, 27 Mar 2021 13:31:44 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Sat, 27 Mar 2021 13:31:44 GMT
ARG SOLR_VERSION=8.8.1
# Sat, 27 Mar 2021 13:31:44 GMT
ARG SOLR_SHA512=a13ad0f8d67e6465d01bd50b9965a042849395e84024cd1093f9e44b9c602ab43b7bbc2f2bc5c1161178ac6bb0c3f717573c69d51baf0aa8f97fb8b5a97a9ffd
# Sat, 27 Mar 2021 13:31:44 GMT
ARG SOLR_KEYS=fbc25d7e1712025294fe66590a6aa179b9bbf45e
# Sat, 27 Mar 2021 13:31:44 GMT
ARG SOLR_DOWNLOAD_URL
# Sat, 27 Mar 2021 13:31:45 GMT
ARG SOLR_DOWNLOAD_SERVER
# Sat, 27 Mar 2021 13:31:51 GMT
# ARGS: SOLR_KEYS=fbc25d7e1712025294fe66590a6aa179b9bbf45e SOLR_SHA512=a13ad0f8d67e6465d01bd50b9965a042849395e84024cd1093f9e44b9c602ab43b7bbc2f2bc5c1161178ac6bb0c3f717573c69d51baf0aa8f97fb8b5a97a9ffd SOLR_VERSION=8.8.1
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Sat, 27 Mar 2021 13:31:51 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.8.1/solr-8.8.1.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.8.1/solr-8.8.1.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.8.1/solr-8.8.1.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Sat, 27 Mar 2021 13:31:52 GMT
# ARGS: SOLR_KEYS=fbc25d7e1712025294fe66590a6aa179b9bbf45e SOLR_SHA512=a13ad0f8d67e6465d01bd50b9965a042849395e84024cd1093f9e44b9c602ab43b7bbc2f2bc5c1161178ac6bb0c3f717573c69d51baf0aa8f97fb8b5a97a9ffd SOLR_VERSION=8.8.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Sat, 27 Mar 2021 13:31:53 GMT
# ARGS: SOLR_KEYS=fbc25d7e1712025294fe66590a6aa179b9bbf45e SOLR_SHA512=a13ad0f8d67e6465d01bd50b9965a042849395e84024cd1093f9e44b9c602ab43b7bbc2f2bc5c1161178ac6bb0c3f717573c69d51baf0aa8f97fb8b5a97a9ffd SOLR_VERSION=8.8.1
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Sat, 27 Mar 2021 13:32:10 GMT
# ARGS: SOLR_KEYS=fbc25d7e1712025294fe66590a6aa179b9bbf45e SOLR_SHA512=a13ad0f8d67e6465d01bd50b9965a042849395e84024cd1093f9e44b9c602ab43b7bbc2f2bc5c1161178ac6bb0c3f717573c69d51baf0aa8f97fb8b5a97a9ffd SOLR_VERSION=8.8.1
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Sat, 27 Mar 2021 13:32:10 GMT
COPY --chown=0:0dir:9bc5f3733a819401f8f06067a2f41713605d2c3bb03bbbe92d04dc2f83bd0265 in /opt/docker-solr/scripts 
# Sat, 27 Mar 2021 13:32:10 GMT
VOLUME [/var/solr]
# Sat, 27 Mar 2021 13:32:11 GMT
EXPOSE 8983
# Sat, 27 Mar 2021 13:32:11 GMT
WORKDIR /opt/solr
# Sat, 27 Mar 2021 13:32:11 GMT
USER solr
# Sat, 27 Mar 2021 13:32:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Mar 2021 13:32:11 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:8bf9c589d5f9475f1fcc050e02308d6b4eeb86eab7752ef948a13693e81a6aaa`  
		Last Modified: Fri, 26 Mar 2021 15:27:11 GMT  
		Size: 50.4 MB (50400278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c70e46d8b5f0e1d77797b7a0565b7a316bd8c7c024f5cca82592128af142dac`  
		Last Modified: Sat, 27 Mar 2021 06:03:41 GMT  
		Size: 7.8 MB (7832558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea848ad42f0d1676b3a0ce709208ba3fa154cd53370c50e7cf8e580c63d96ae0`  
		Last Modified: Sat, 27 Mar 2021 06:03:41 GMT  
		Size: 10.0 MB (9997159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353a86a0b8e31a5bace7a3688353fbc7d4f597f13e3ed60101fe78c7f47c6750`  
		Last Modified: Sat, 27 Mar 2021 13:01:39 GMT  
		Size: 5.5 MB (5531058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de31561d106bbcb5b6a7cd9a46caa49ea0d672cced8eb94d58845fb7832aa3e1`  
		Last Modified: Sat, 27 Mar 2021 13:01:39 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39470804b1440c1955af4eb429e98e2ca8d6992950dbc8c7d476be5c1d949c80`  
		Last Modified: Sat, 27 Mar 2021 13:01:47 GMT  
		Size: 46.8 MB (46760609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c77cf7aed908d9dad2823da451adfff629aff031c3ea8fa2f3af34bf3a82c2c`  
		Last Modified: Sat, 27 Mar 2021 13:42:53 GMT  
		Size: 2.5 MB (2546166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3013720e5305a56da2f2d9d36779e61834b85c87e63b06f0ac1e9264288f41b8`  
		Last Modified: Sat, 27 Mar 2021 13:42:52 GMT  
		Size: 4.3 KB (4283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c60daa2a3fa30e1a688852431c4973e560b58abc81ff983590c1a1e5615f87f`  
		Last Modified: Sat, 27 Mar 2021 13:42:52 GMT  
		Size: 2.9 KB (2926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f73b1c3b1e397cc0c7c3c4ef2f9566045a7721e0b04948bdae6a6dde05de96`  
		Last Modified: Sat, 27 Mar 2021 13:43:05 GMT  
		Size: 196.5 MB (196497933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfde0a9e471d51eb31461d505c00e26c6d0bcad450bec3912a9079644a25c83a`  
		Last Modified: Sat, 27 Mar 2021 13:42:52 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:bb64667f91264fd8e7cb4794737af969994ec22657354cb7e06a914b2dbad359
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.2 MB (317196190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72709d1f28995620c0b65c63a2cae06022b7395743b472f742ee61ed79980489`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 26 Mar 2021 15:41:27 GMT
ADD file:536306ac674764a6a921b71adcbb4440797b916a0583b9270cd1565d62642e4d in / 
# Fri, 26 Mar 2021 15:41:30 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 04:14:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 04:14:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 10:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 10:44:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 27 Mar 2021 10:44:34 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 27 Mar 2021 10:44:35 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Mar 2021 10:44:36 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 10:44:36 GMT
ENV JAVA_VERSION=11.0.10
# Sat, 27 Mar 2021 10:44:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_x64_linux_11.0.10_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_aarch64_linux_11.0.10_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 27 Mar 2021 11:10:05 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Sat, 27 Mar 2021 11:10:06 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Sat, 27 Mar 2021 11:10:07 GMT
ARG SOLR_VERSION=8.8.1
# Sat, 27 Mar 2021 11:10:07 GMT
ARG SOLR_SHA512=a13ad0f8d67e6465d01bd50b9965a042849395e84024cd1093f9e44b9c602ab43b7bbc2f2bc5c1161178ac6bb0c3f717573c69d51baf0aa8f97fb8b5a97a9ffd
# Sat, 27 Mar 2021 11:10:08 GMT
ARG SOLR_KEYS=fbc25d7e1712025294fe66590a6aa179b9bbf45e
# Sat, 27 Mar 2021 11:10:09 GMT
ARG SOLR_DOWNLOAD_URL
# Sat, 27 Mar 2021 11:10:11 GMT
ARG SOLR_DOWNLOAD_SERVER
# Sat, 27 Mar 2021 11:10:24 GMT
# ARGS: SOLR_KEYS=fbc25d7e1712025294fe66590a6aa179b9bbf45e SOLR_SHA512=a13ad0f8d67e6465d01bd50b9965a042849395e84024cd1093f9e44b9c602ab43b7bbc2f2bc5c1161178ac6bb0c3f717573c69d51baf0aa8f97fb8b5a97a9ffd SOLR_VERSION=8.8.1
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Sat, 27 Mar 2021 11:10:27 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.8.1/solr-8.8.1.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.8.1/solr-8.8.1.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.8.1/solr-8.8.1.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Sat, 27 Mar 2021 11:10:34 GMT
# ARGS: SOLR_KEYS=fbc25d7e1712025294fe66590a6aa179b9bbf45e SOLR_SHA512=a13ad0f8d67e6465d01bd50b9965a042849395e84024cd1093f9e44b9c602ab43b7bbc2f2bc5c1161178ac6bb0c3f717573c69d51baf0aa8f97fb8b5a97a9ffd SOLR_VERSION=8.8.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Sat, 27 Mar 2021 11:10:39 GMT
# ARGS: SOLR_KEYS=fbc25d7e1712025294fe66590a6aa179b9bbf45e SOLR_SHA512=a13ad0f8d67e6465d01bd50b9965a042849395e84024cd1093f9e44b9c602ab43b7bbc2f2bc5c1161178ac6bb0c3f717573c69d51baf0aa8f97fb8b5a97a9ffd SOLR_VERSION=8.8.1
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Sat, 27 Mar 2021 11:12:18 GMT
# ARGS: SOLR_KEYS=fbc25d7e1712025294fe66590a6aa179b9bbf45e SOLR_SHA512=a13ad0f8d67e6465d01bd50b9965a042849395e84024cd1093f9e44b9c602ab43b7bbc2f2bc5c1161178ac6bb0c3f717573c69d51baf0aa8f97fb8b5a97a9ffd SOLR_VERSION=8.8.1
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Sat, 27 Mar 2021 11:12:20 GMT
COPY --chown=0:0dir:9bc5f3733a819401f8f06067a2f41713605d2c3bb03bbbe92d04dc2f83bd0265 in /opt/docker-solr/scripts 
# Sat, 27 Mar 2021 11:12:21 GMT
VOLUME [/var/solr]
# Sat, 27 Mar 2021 11:12:23 GMT
EXPOSE 8983
# Sat, 27 Mar 2021 11:12:24 GMT
WORKDIR /opt/solr
# Sat, 27 Mar 2021 11:12:25 GMT
USER solr
# Sat, 27 Mar 2021 11:12:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Mar 2021 11:12:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:383261dafcc4f63ecae5f2d661d1ef8d0a5e1c9f4b1f12285115baca7d101d5a`  
		Last Modified: Fri, 26 Mar 2021 15:48:21 GMT  
		Size: 49.2 MB (49196215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a8073d5d993eeeb13d2b5798a56220bed01add2f8e543d1a68cf5bdeb13b3a`  
		Last Modified: Sat, 27 Mar 2021 04:28:03 GMT  
		Size: 7.7 MB (7694449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e04ac5d1463667a0a3b2db65c9975df4dda175b8d5442808d4b141537d5531`  
		Last Modified: Sat, 27 Mar 2021 04:28:03 GMT  
		Size: 10.0 MB (9984376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46261e8de28d17c0bdc28d8553bff431d985f6194cb454ab7858dcc7d4a2d2ee`  
		Last Modified: Sat, 27 Mar 2021 10:49:59 GMT  
		Size: 5.5 MB (5505625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5fd41bd0a2089d7c9b9fb13768e54c6a96034aff3aebd9838b069948cba74d`  
		Last Modified: Sat, 27 Mar 2021 10:49:58 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03a65005c4eb64872df1cc57b2d7a457d18db92f6e9fcbceb5f0a6984367949`  
		Last Modified: Sat, 27 Mar 2021 10:50:11 GMT  
		Size: 45.8 MB (45839784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4229a4eed248761decdfdda196aba342c72fe7313eb0a5715a9580d8298c8a66`  
		Last Modified: Sat, 27 Mar 2021 11:23:52 GMT  
		Size: 2.5 MB (2464057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98d145a6ee761b355e505b368fc5e6d001e7d7896cf18b86f72cc7e708c7569`  
		Last Modified: Sat, 27 Mar 2021 11:23:51 GMT  
		Size: 4.3 KB (4325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76b05db3bb09f572dfdb15ba38359f3c2fd1af5767da385060caebcb235be41`  
		Last Modified: Sat, 27 Mar 2021 11:23:51 GMT  
		Size: 2.9 KB (2913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0edf29b4d4b1a7caff5d589ff77563cdce26372e78ab60f1879f1cc27e2278f`  
		Last Modified: Sat, 27 Mar 2021 11:24:13 GMT  
		Size: 196.5 MB (196497956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b50e83788d9f91a2cdcd4ddfe7724674b18a4f2ad26f116f647f4bb18bfde8`  
		Last Modified: Sat, 27 Mar 2021 11:23:51 GMT  
		Size: 6.3 KB (6277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
