## `solr:slim`

```console
$ docker pull solr@sha256:568c85fa34a46bbd4cac39967908d57cdfb37668e0b59abe9ca7eebdd7f58e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `solr:slim` - linux; amd64

```console
$ docker pull solr@sha256:2a177191cf2bdf1426738681946219c35b76b898c9a6c29110a75498ce9b074a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.2 MB (305202398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fecc00cf387b32ad52eee39f0267fe5cf6161839f38b48acccf39a5cc5649f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:34:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:34:58 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:34:58 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:34:59 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:34:59 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:37:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Fri, 03 Dec 2021 15:32:52 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Fri, 03 Dec 2021 15:32:52 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Fri, 17 Dec 2021 19:39:01 GMT
ARG SOLR_VERSION=8.11.1
# Fri, 17 Dec 2021 19:39:01 GMT
ARG SOLR_SHA512=4893f836aec84b03d7bfe574e59e305c03b5ede4a48020034fbe81440b8feee79e55fd9ead230e5b89b3f25124e9b56c1ddc4bb5c7f631cf4e846b9cab5f9a45
# Fri, 17 Dec 2021 19:39:01 GMT
ARG SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E
# Fri, 17 Dec 2021 19:39:01 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 17 Dec 2021 19:39:02 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 17 Dec 2021 19:39:13 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=4893f836aec84b03d7bfe574e59e305c03b5ede4a48020034fbe81440b8feee79e55fd9ead230e5b89b3f25124e9b56c1ddc4bb5c7f631cf4e846b9cab5f9a45 SOLR_VERSION=8.11.1
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Fri, 17 Dec 2021 19:39:13 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.1/solr-8.11.1.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.1/solr-8.11.1.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.1/solr-8.11.1.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Fri, 17 Dec 2021 19:39:15 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=4893f836aec84b03d7bfe574e59e305c03b5ede4a48020034fbe81440b8feee79e55fd9ead230e5b89b3f25124e9b56c1ddc4bb5c7f631cf4e846b9cab5f9a45 SOLR_VERSION=8.11.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 17 Dec 2021 19:39:19 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=4893f836aec84b03d7bfe574e59e305c03b5ede4a48020034fbe81440b8feee79e55fd9ead230e5b89b3f25124e9b56c1ddc4bb5c7f631cf4e846b9cab5f9a45 SOLR_VERSION=8.11.1
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Fri, 17 Dec 2021 19:39:53 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=4893f836aec84b03d7bfe574e59e305c03b5ede4a48020034fbe81440b8feee79e55fd9ead230e5b89b3f25124e9b56c1ddc4bb5c7f631cf4e846b9cab5f9a45 SOLR_VERSION=8.11.1
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Fri, 17 Dec 2021 19:39:54 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Fri, 17 Dec 2021 19:39:54 GMT
VOLUME [/var/solr]
# Fri, 17 Dec 2021 19:39:54 GMT
EXPOSE 8983
# Fri, 17 Dec 2021 19:39:55 GMT
WORKDIR /opt/solr
# Fri, 17 Dec 2021 19:39:55 GMT
USER solr
# Fri, 17 Dec 2021 19:39:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Dec 2021 19:39:55 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9f5b9b70c2f137dc70e816256e7a568a084d066e7c34c028d30a6a45438685`  
		Last Modified: Thu, 02 Dec 2021 11:47:20 GMT  
		Size: 1.6 MB (1582045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487fc3d77b36e6ef6949adfd74769b0d393dec1d06fa2657f03911fcba2b0323`  
		Last Modified: Thu, 02 Dec 2021 11:55:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945725b52efd3fe6ccf97fe0093f8e1ab51ea777f7d337b8f19198cde74903d0`  
		Last Modified: Thu, 02 Dec 2021 11:58:16 GMT  
		Size: 47.1 MB (47104036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3fefa90465e3ed27eceefcec60857dd097a619395f3ebceba033340b60dd1f`  
		Last Modified: Fri, 17 Dec 2021 19:42:42 GMT  
		Size: 6.9 MB (6898128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4735b1025e9417b10765af6baa09b84e147dc6969cc44d098ce3d2f5aa7f7eed`  
		Last Modified: Fri, 17 Dec 2021 19:42:41 GMT  
		Size: 4.3 KB (4289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7524c73f2364e0ce41a81c398558ba5388f46acf8f489665d7f7a7c5dba6a092`  
		Last Modified: Fri, 17 Dec 2021 19:42:41 GMT  
		Size: 5.1 KB (5108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72359590fc01b74e8859da27ff600d52c9a63d3b27589a3a767f607a4c4f375`  
		Last Modified: Fri, 17 Dec 2021 19:42:53 GMT  
		Size: 218.2 MB (218232054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb6d8694001a6a586f550d33417dcd2936e8d2a15f79ce3bc5aa8a7f79838fb`  
		Last Modified: Fri, 17 Dec 2021 19:42:41 GMT  
		Size: 6.3 KB (6308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:424e1a40c32c73c2115674d797f9d547ef531d0ad519b2826acc6c6ba72e289e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302236916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb8d5adcbc92f03eea192bdb60d65532af2a160242886bc71eb7bfd8830b42a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:02:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:08:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 02 Dec 2021 11:08:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 02 Dec 2021 11:08:01 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:08:02 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:08:03 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 02 Dec 2021 11:10:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Fri, 03 Dec 2021 06:47:39 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Fri, 03 Dec 2021 06:47:40 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Fri, 17 Dec 2021 19:12:46 GMT
ARG SOLR_VERSION=8.11.1
# Fri, 17 Dec 2021 19:12:47 GMT
ARG SOLR_SHA512=4893f836aec84b03d7bfe574e59e305c03b5ede4a48020034fbe81440b8feee79e55fd9ead230e5b89b3f25124e9b56c1ddc4bb5c7f631cf4e846b9cab5f9a45
# Fri, 17 Dec 2021 19:12:48 GMT
ARG SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E
# Fri, 17 Dec 2021 19:12:49 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 17 Dec 2021 19:12:50 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 17 Dec 2021 19:12:58 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=4893f836aec84b03d7bfe574e59e305c03b5ede4a48020034fbe81440b8feee79e55fd9ead230e5b89b3f25124e9b56c1ddc4bb5c7f631cf4e846b9cab5f9a45 SOLR_VERSION=8.11.1
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Fri, 17 Dec 2021 19:12:58 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.11.1/solr-8.11.1.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.11.1/solr-8.11.1.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.11.1/solr-8.11.1.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Fri, 17 Dec 2021 19:12:59 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=4893f836aec84b03d7bfe574e59e305c03b5ede4a48020034fbe81440b8feee79e55fd9ead230e5b89b3f25124e9b56c1ddc4bb5c7f631cf4e846b9cab5f9a45 SOLR_VERSION=8.11.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 17 Dec 2021 19:13:02 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=4893f836aec84b03d7bfe574e59e305c03b5ede4a48020034fbe81440b8feee79e55fd9ead230e5b89b3f25124e9b56c1ddc4bb5c7f631cf4e846b9cab5f9a45 SOLR_VERSION=8.11.1
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Fri, 17 Dec 2021 19:14:28 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=4893f836aec84b03d7bfe574e59e305c03b5ede4a48020034fbe81440b8feee79e55fd9ead230e5b89b3f25124e9b56c1ddc4bb5c7f631cf4e846b9cab5f9a45 SOLR_VERSION=8.11.1
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Fri, 17 Dec 2021 19:14:29 GMT
COPY --chown=0:0dir:fa78a99fcb12fc7f149f5ca608174160823420c330ad466b81ecc42bac19f7d6 in /opt/docker-solr/scripts 
# Fri, 17 Dec 2021 19:14:29 GMT
VOLUME [/var/solr]
# Fri, 17 Dec 2021 19:14:30 GMT
EXPOSE 8983
# Fri, 17 Dec 2021 19:14:31 GMT
WORKDIR /opt/solr
# Fri, 17 Dec 2021 19:14:32 GMT
USER solr
# Fri, 17 Dec 2021 19:14:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Dec 2021 19:14:34 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595058421fcb005f80f2faa2434369885cb20645caed265e7b4912808701d893`  
		Last Modified: Thu, 02 Dec 2021 11:23:15 GMT  
		Size: 1.4 MB (1361242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847c13000ac6e7eb05246ab778901565fb6666b6250d9e32b84ce2fa07be4b85`  
		Last Modified: Thu, 02 Dec 2021 11:31:49 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1a952c2ccfde12b2df888bd2d747561ab4fa9d55cee78436f8cdeee20c955b`  
		Last Modified: Thu, 02 Dec 2021 11:34:39 GMT  
		Size: 46.0 MB (45975727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1c13a10547619adca08b47815365de38aa15cfd207d20289081b76d32117cd`  
		Last Modified: Fri, 17 Dec 2021 19:18:44 GMT  
		Size: 6.6 MB (6597715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1e61aac4761935ffefab1cc5ea74c72be35efdc82b6c4f7df25eae326415b5`  
		Last Modified: Fri, 17 Dec 2021 19:18:43 GMT  
		Size: 4.2 KB (4203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512432ea2989d80e64a0777a1e4c6e41a05eda223d6262394c4b68b7bbbc53e`  
		Last Modified: Fri, 17 Dec 2021 19:18:44 GMT  
		Size: 4.5 KB (4540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f10f0b83f4387c8a5a5c974d5929856910550bb0b08a9da33b07e1c7610012c`  
		Last Modified: Fri, 17 Dec 2021 19:19:01 GMT  
		Size: 218.2 MB (218230465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3017d7185c2b987581351723b9df4d11122fe65d668f11d695d3f144c2510c00`  
		Last Modified: Fri, 17 Dec 2021 19:18:43 GMT  
		Size: 6.3 KB (6279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
