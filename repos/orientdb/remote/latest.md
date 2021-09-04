## `orientdb:latest`

```console
$ docker pull orientdb@sha256:e4d88b20ee11be5a2401aa62bbad1f7add1e0d16af75aafd0c7bf8f7c45fd13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:6a7eb1991ba9fbd10fe50904bd127f8114f96ddc99b71cd36a14f34b177a048d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211537254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656251abb9b8567abbda1d22b62687fda4c5375107d4f6b8dff6b3a55db86e8d`
-	Default Command: `["server.sh"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:21 GMT
ADD file:19d7ba0fceddd7fc78b5fb96cf8110e5d10e0e5d2554030dfe640d161379cb79 in / 
# Fri, 03 Sep 2021 01:21:21 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:31:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:41:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Fri, 03 Sep 2021 08:41:29 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Fri, 03 Sep 2021 08:41:29 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Sep 2021 08:41:29 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:41:29 GMT
ENV JAVA_VERSION=8u302
# Fri, 03 Sep 2021 08:41:46 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sat, 04 Sep 2021 12:25:03 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sat, 04 Sep 2021 12:25:03 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sat, 04 Sep 2021 12:25:04 GMT
ENV ORIENTDB_VERSION=3.2.0
# Sat, 04 Sep 2021 12:25:04 GMT
ENV ORIENTDB_DOWNLOAD_MD5=7bff911bea6b02d2f1d9ddff5e4ba8ea
# Sat, 04 Sep 2021 12:25:04 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=f424731e3d078de692fab97d6aa3b3e8395d7d01
# Sat, 04 Sep 2021 12:25:04 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.2.0/orientdb-community-3.2.0.tar.gz
# Sat, 04 Sep 2021 12:25:09 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Sep 2021 12:25:14 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sat, 04 Sep 2021 12:25:14 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Sep 2021 12:25:14 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sat, 04 Sep 2021 12:25:15 GMT
WORKDIR /orientdb
# Sat, 04 Sep 2021 12:25:15 GMT
EXPOSE 2424
# Sat, 04 Sep 2021 12:25:15 GMT
EXPOSE 2480
# Sat, 04 Sep 2021 12:25:15 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:f8416d8bac72cefc0ce17bd2dc0c03aa43e123d309db92ee23be9382192cf2ed`  
		Last Modified: Fri, 03 Sep 2021 01:27:25 GMT  
		Size: 31.4 MB (31368702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ae0b0c4c13e1ebacfd091b8e226cc8aa92df8937632e3bec2b03a877bf2d87`  
		Last Modified: Fri, 03 Sep 2021 08:49:03 GMT  
		Size: 1.6 MB (1582002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098f9d3d8dab5a269d2e9252501b6c6d034bcb6debc0e8e7cb388002034df175`  
		Last Modified: Fri, 03 Sep 2021 09:05:50 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85bd97f1dba1d1c9adb7383afa4ff1f571593dbf1ee23bd74b43beb994743c3d`  
		Last Modified: Fri, 03 Sep 2021 09:06:01 GMT  
		Size: 106.3 MB (106261868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c26919469a72e2eaad2e93094097651f8d8e6ed66e16e632296cc7acbdc129`  
		Last Modified: Sat, 04 Sep 2021 12:27:38 GMT  
		Size: 2.1 MB (2102014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803f9115e4555781736441b12843beb0777b9a4ad9c339eda315391e6a954692`  
		Last Modified: Sat, 04 Sep 2021 12:27:42 GMT  
		Size: 70.2 MB (70222460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
