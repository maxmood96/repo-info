## `orientdb:latest`

```console
$ docker pull orientdb@sha256:4c5ced5998cf2f972304eb94bb8809f3cb2a0a306ea14c146a1646ad796e48fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:351dbd9fc4dbc9666ea791122fc4e74edc819b85448b7c1537febc8e6c52e915
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (214036296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ce267ccf1c0ee0fe53cc5d4844adefb61caf61f551be9b179179f56849d34c`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 02:20:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 02:20:39 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 02:20:40 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 02:20:40 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 02:20:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 28 May 2022 23:28:16 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 28 May 2022 23:28:16 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_VERSION=3.2.6
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_DOWNLOAD_MD5=08e39080df862d3c5570f834d9d6f92b
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=ba07e961cd05dfe2d3bc623e865ae21e533ace68
# Sat, 28 May 2022 23:28:16 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.6/orientdb-community-3.2.6.tar.gz
# Sat, 28 May 2022 23:28:20 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 23:28:27 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 28 May 2022 23:28:27 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 23:28:27 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 28 May 2022 23:28:28 GMT
WORKDIR /orientdb
# Sat, 28 May 2022 23:28:28 GMT
EXPOSE 2424
# Sat, 28 May 2022 23:28:28 GMT
EXPOSE 2480
# Sat, 28 May 2022 23:28:28 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b062e78fd7c8f9370711c8b47595bc59fea38f7e04e22d887fbd3256f2324c`  
		Last Modified: Sat, 28 May 2022 02:27:46 GMT  
		Size: 1.6 MB (1582290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee8efac34e15a189c9415d5c98b91644e4e1cfdb6aa359f5b80fbca3ddcbcc`  
		Last Modified: Sat, 28 May 2022 02:34:30 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cb291159d768eadbf26f320fd580e1f48dd39ec6ac1c25e536bedce86365fe`  
		Last Modified: Sat, 28 May 2022 02:34:40 GMT  
		Size: 106.2 MB (106215398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81e24edbfb36ef2f8fb16c818dfb34e807fa0a85811c72faafa7edd04532306`  
		Last Modified: Sat, 28 May 2022 23:30:33 GMT  
		Size: 2.1 MB (2105667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3277f8b93337b3b310a6c83af66aa211cc0842a759530541bcf77a24f39dabd8`  
		Last Modified: Sat, 28 May 2022 23:30:37 GMT  
		Size: 72.8 MB (72753454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
