## `orientdb:latest`

```console
$ docker pull orientdb@sha256:c1ca7257ac10cb1c99058a4e18c2ef1c434a8f2aeeec27c3b18d2cbebee1b64a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `orientdb:latest` - linux; amd64

```console
$ docker pull orientdb@sha256:4bc1fa5d978f29ee837d2ec0e6885e1f2c003ea9dc8e4fe7aab4abd47f9c22d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191660924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca8104f46baca1c76232a8a908b81250b710ad71ebe6c7bb5aee952ef22a3be`
-	Default Command: `["server.sh"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:49:19 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 10 Apr 2021 12:49:20 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 10 Apr 2021 12:49:20 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 12:49:20 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:49:20 GMT
ENV JAVA_VERSION=8u282
# Sat, 10 Apr 2021 12:49:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/jre/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		javac -version; 	java -version
# Sun, 11 Apr 2021 03:15:53 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Sun, 11 Apr 2021 03:15:53 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Sun, 11 Apr 2021 03:15:53 GMT
ENV ORIENTDB_VERSION=3.1.10
# Sun, 11 Apr 2021 03:15:53 GMT
ENV ORIENTDB_DOWNLOAD_MD5=0bcdf23fb4e8d4647aa74730cc4212af
# Sun, 11 Apr 2021 03:15:53 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=e6aa30b22169315c2a7420c2a862775c62cedafc
# Sun, 11 Apr 2021 03:15:54 GMT
ENV ORIENTDB_DOWNLOAD_URL=https://repo1.maven.org/maven2/com/orientechnologies/orientdb-community/3.1.10/orientdb-community-3.1.10.tar.gz
# Sun, 11 Apr 2021 03:15:59 GMT
RUN apt update     && apt install -y curl wget     && rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 03:16:03 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Sun, 11 Apr 2021 03:16:03 GMT
ENV PATH=/orientdb/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 11 Apr 2021 03:16:04 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Sun, 11 Apr 2021 03:16:04 GMT
WORKDIR /orientdb
# Sun, 11 Apr 2021 03:16:04 GMT
EXPOSE 2424
# Sun, 11 Apr 2021 03:16:04 GMT
EXPOSE 2480
# Sun, 11 Apr 2021 03:16:04 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf4c47c8c6124c3089f3ed26410da9870ba18dd4bc68331e2b7e853116a6cad`  
		Last Modified: Sat, 10 Apr 2021 12:54:28 GMT  
		Size: 3.3 MB (3268764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636165fc8c7051310a4652b5eb422703a59321f36f8e802272d196d11a54e37c`  
		Last Modified: Sat, 10 Apr 2021 13:02:04 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9872178e0d4c6bfd19057ec53cd38807e271d7324bdc1afc7289cac83e8f503`  
		Last Modified: Sat, 10 Apr 2021 13:02:17 GMT  
		Size: 106.2 MB (106187751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52b1c342172b07e2a059c2900ee42867adbfe81a2c9f7bf1ec7f4a2af3a429e`  
		Last Modified: Sun, 11 Apr 2021 03:18:05 GMT  
		Size: 2.6 MB (2615919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cbd8ea139f216caf6131e2b406092e38e7587b42a817be5450704685c6714d7`  
		Last Modified: Sun, 11 Apr 2021 03:18:13 GMT  
		Size: 52.4 MB (52448907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
