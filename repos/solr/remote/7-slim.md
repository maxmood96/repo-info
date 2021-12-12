## `solr:7-slim`

```console
$ docker pull solr@sha256:398d1f6b1846f1f4e87b27cc3a9425d9a2dc29392a72d1d273465566b54c83a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `solr:7-slim` - linux; amd64

```console
$ docker pull solr@sha256:c203de56ab9705f5e705753dcee403fbc2a995ce13f4807fd2941135dfab7e85
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258483188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c038312a0762d4bb1e7f10ed767c8e01e862f843c99cb6601c1a6158eb4556`
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
# Fri, 03 Dec 2021 15:52:27 GMT
ARG SOLR_VERSION=7.7.3
# Fri, 03 Dec 2021 15:52:28 GMT
ARG SOLR_SHA512=ca9200c18cc19ab723fd4d10f257e27eb81dc8bc33401ebc4eb99178faf4033a2684f0f8b12ae7b659cfeb0f4c9d9e24aaac518a4e00fd28b69854a359a666ed
# Fri, 03 Dec 2021 15:52:28 GMT
ARG SOLR_KEYS=CFCE5FBB920C3C745CEEE084C38FF5EC3FCFDB3E
# Fri, 03 Dec 2021 15:52:28 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 03 Dec 2021 15:52:28 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 03 Dec 2021 15:52:36 GMT
# ARGS: SOLR_KEYS=CFCE5FBB920C3C745CEEE084C38FF5EC3FCFDB3E SOLR_SHA512=ca9200c18cc19ab723fd4d10f257e27eb81dc8bc33401ebc4eb99178faf4033a2684f0f8b12ae7b659cfeb0f4c9d9e24aaac518a4e00fd28b69854a359a666ed SOLR_VERSION=7.7.3
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Fri, 03 Dec 2021 15:52:36 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/7.7.3/solr-7.7.3.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/7.7.3/solr-7.7.3.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/7.7.3/solr-7.7.3.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 15:52:37 GMT
# ARGS: SOLR_KEYS=CFCE5FBB920C3C745CEEE084C38FF5EC3FCFDB3E SOLR_SHA512=ca9200c18cc19ab723fd4d10f257e27eb81dc8bc33401ebc4eb99178faf4033a2684f0f8b12ae7b659cfeb0f4c9d9e24aaac518a4e00fd28b69854a359a666ed SOLR_VERSION=7.7.3
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 03 Dec 2021 15:52:39 GMT
# ARGS: SOLR_KEYS=CFCE5FBB920C3C745CEEE084C38FF5EC3FCFDB3E SOLR_SHA512=ca9200c18cc19ab723fd4d10f257e27eb81dc8bc33401ebc4eb99178faf4033a2684f0f8b12ae7b659cfeb0f4c9d9e24aaac518a4e00fd28b69854a359a666ed SOLR_VERSION=7.7.3
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Fri, 03 Dec 2021 15:52:47 GMT
# ARGS: SOLR_KEYS=CFCE5FBB920C3C745CEEE084C38FF5EC3FCFDB3E SOLR_SHA512=ca9200c18cc19ab723fd4d10f257e27eb81dc8bc33401ebc4eb99178faf4033a2684f0f8b12ae7b659cfeb0f4c9d9e24aaac518a4e00fd28b69854a359a666ed SOLR_VERSION=7.7.3
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   mv "/opt/solr-$SOLR_VERSION" /opt/solr;   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   mkdir -p /opt/solr/server/solr/mycores /opt/solr/server/logs /opt/mysolrhome;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   if [ -f "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter" ]; then chmod 0755 "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter"; fi;   chmod -R 0755 /opt/solr/server/scripts/cloud-scripts;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/solr /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/mysolrhome;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Sun, 12 Dec 2021 06:21:41 GMT
COPY --chown=solr:solrdir:47673e85b88ff0771446ce93142f786f59e74a0232d547ae66ced7f9058c0a14 in /opt/docker-solr/scripts 
# Sun, 12 Dec 2021 06:21:41 GMT
EXPOSE 8983
# Sun, 12 Dec 2021 06:21:41 GMT
WORKDIR /opt/solr
# Sun, 12 Dec 2021 06:21:41 GMT
USER solr
# Sun, 12 Dec 2021 06:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 12 Dec 2021 06:21:42 GMT
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
	-	`sha256:8fd76d1846d1a46edd69cca4557bfea101593315a5ec05b6dae5d06f4bf6d572`  
		Last Modified: Fri, 03 Dec 2021 16:05:39 GMT  
		Size: 6.9 MB (6898084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb9128b7a256c6589cfc0d421e0dda3644f0ad6a48009a2ef0da5cc6642d22`  
		Last Modified: Fri, 03 Dec 2021 16:05:38 GMT  
		Size: 4.3 KB (4285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae100e1f484e3f5a028bed9200ea2ea684e886d38601427113fb2faddd039e3d`  
		Last Modified: Fri, 03 Dec 2021 16:05:38 GMT  
		Size: 2.9 KB (2909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6396994d9d146b705166f2a7a5b1effe28cec4640c7b2ff43753dd8f4b2af15`  
		Last Modified: Fri, 03 Dec 2021 16:05:47 GMT  
		Size: 171.5 MB (171515278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8d9bd4ffa92785830a5c0fc4ce4925d69ed3fd833e7792770a6e1cbea10b65`  
		Last Modified: Sun, 12 Dec 2021 06:27:33 GMT  
		Size: 6.1 KB (6121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:7-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:63ce3f68ea414c18a177f9db65f87e539aeaa0b61eec2aefafd0e019c57e0d67
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255525007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495ee7fd020241d8f373ee5e1a1374fa121358f5cf59a18f2ed9eb39ce61657b`
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
# Fri, 03 Dec 2021 07:16:11 GMT
ARG SOLR_VERSION=7.7.3
# Fri, 03 Dec 2021 07:16:12 GMT
ARG SOLR_SHA512=ca9200c18cc19ab723fd4d10f257e27eb81dc8bc33401ebc4eb99178faf4033a2684f0f8b12ae7b659cfeb0f4c9d9e24aaac518a4e00fd28b69854a359a666ed
# Fri, 03 Dec 2021 07:16:13 GMT
ARG SOLR_KEYS=CFCE5FBB920C3C745CEEE084C38FF5EC3FCFDB3E
# Fri, 03 Dec 2021 07:16:14 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 03 Dec 2021 07:16:15 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 03 Dec 2021 07:16:22 GMT
# ARGS: SOLR_KEYS=CFCE5FBB920C3C745CEEE084C38FF5EC3FCFDB3E SOLR_SHA512=ca9200c18cc19ab723fd4d10f257e27eb81dc8bc33401ebc4eb99178faf4033a2684f0f8b12ae7b659cfeb0f4c9d9e24aaac518a4e00fd28b69854a359a666ed SOLR_VERSION=7.7.3
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Fri, 03 Dec 2021 07:16:23 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/7.7.3/solr-7.7.3.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/7.7.3/solr-7.7.3.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/7.7.3/solr-7.7.3.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 07:16:24 GMT
# ARGS: SOLR_KEYS=CFCE5FBB920C3C745CEEE084C38FF5EC3FCFDB3E SOLR_SHA512=ca9200c18cc19ab723fd4d10f257e27eb81dc8bc33401ebc4eb99178faf4033a2684f0f8b12ae7b659cfeb0f4c9d9e24aaac518a4e00fd28b69854a359a666ed SOLR_VERSION=7.7.3
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 03 Dec 2021 07:16:26 GMT
# ARGS: SOLR_KEYS=CFCE5FBB920C3C745CEEE084C38FF5EC3FCFDB3E SOLR_SHA512=ca9200c18cc19ab723fd4d10f257e27eb81dc8bc33401ebc4eb99178faf4033a2684f0f8b12ae7b659cfeb0f4c9d9e24aaac518a4e00fd28b69854a359a666ed SOLR_VERSION=7.7.3
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Fri, 03 Dec 2021 07:16:35 GMT
# ARGS: SOLR_KEYS=CFCE5FBB920C3C745CEEE084C38FF5EC3FCFDB3E SOLR_SHA512=ca9200c18cc19ab723fd4d10f257e27eb81dc8bc33401ebc4eb99178faf4033a2684f0f8b12ae7b659cfeb0f4c9d9e24aaac518a4e00fd28b69854a359a666ed SOLR_VERSION=7.7.3
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   mv "/opt/solr-$SOLR_VERSION" /opt/solr;   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   mkdir -p /opt/solr/server/solr/mycores /opt/solr/server/logs /opt/mysolrhome;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   if [ -f "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter" ]; then chmod 0755 "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter"; fi;   chmod -R 0755 /opt/solr/server/scripts/cloud-scripts;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/solr /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/mysolrhome;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Sun, 12 Dec 2021 05:48:29 GMT
COPY --chown=solr:solrdir:47673e85b88ff0771446ce93142f786f59e74a0232d547ae66ced7f9058c0a14 in /opt/docker-solr/scripts 
# Sun, 12 Dec 2021 05:48:29 GMT
EXPOSE 8983
# Sun, 12 Dec 2021 05:48:30 GMT
WORKDIR /opt/solr
# Sun, 12 Dec 2021 05:48:31 GMT
USER solr
# Sun, 12 Dec 2021 05:48:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 12 Dec 2021 05:48:33 GMT
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
	-	`sha256:a591fa8d9aa7daf648bb9eb5df3a00e22847f563fb97d035cbc06ee5b5207a55`  
		Last Modified: Fri, 03 Dec 2021 10:28:06 GMT  
		Size: 6.6 MB (6597704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be8314cc5d948dd3bb04f796b1d8eaaac77a20a26c08c68291c94fff3b9c7d8`  
		Last Modified: Fri, 03 Dec 2021 10:28:04 GMT  
		Size: 4.2 KB (4198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b632be475091bbbd464a54d899d664638c8cb216cb94da54093d27a9d6224b4`  
		Last Modified: Fri, 03 Dec 2021 10:28:04 GMT  
		Size: 2.9 KB (2882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d24150c324fb28919cacdab919d4a870309ca7cdb0476e2267b499592583270`  
		Last Modified: Fri, 03 Dec 2021 10:28:16 GMT  
		Size: 171.5 MB (171520423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5aa7d3d573458e1679fcdb31862391aadae98f4cbf4f2eb4d027d4a2a4c663`  
		Last Modified: Sun, 12 Dec 2021 05:55:18 GMT  
		Size: 6.1 KB (6086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
