## `openjdk:20-ea-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:f6b6c3a2b1762d30b9d44ad995792111aa7cae9057640919f2225c47c99d1d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:0ef1c231613de907b7e980a198cb79eb8a8768c87bbd70c0df91ab2afce6c342
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228914346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320e7f3ada92da205461226473517d25f88226e11f8f9efa889324f85a2066e0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 07:04:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 07:06:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Wed, 11 Jan 2023 07:06:17 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 07:06:17 GMT
ENV LANG=C.UTF-8
# Mon, 30 Jan 2023 19:23:06 GMT
ENV JAVA_VERSION=20-ea+33
# Mon, 30 Jan 2023 19:23:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/33/GPL/openjdk-20-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='60a22410863626139939d3bcbb04c01d8aafaf666c8a61532ec7fa6d5a3f90b3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/33/GPL/openjdk-20-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='cd944c1f8b593e18f863d36262b710bcaccf05f28c4a02a6cf01d3ad7fcc2f68'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 30 Jan 2023 19:23:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828545e8b79db162ad5abac22f03044bd33fdec65ab2de0eab43a39483567a11`  
		Last Modified: Wed, 11 Jan 2023 07:12:21 GMT  
		Size: 3.3 MB (3275922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3f081643ab4055e18086fc77713b9927b31c64ada0258256348c5e23bcebc4`  
		Last Modified: Mon, 30 Jan 2023 19:33:23 GMT  
		Size: 198.5 MB (198498072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:195ee66b51ac84663fa42daaf1c98196b40ea9310b3afda1434e6ddd626404a7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226057682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2878260bfefa372829c36a071dd7f9d60c55887fe370cca240ecb22d0d2663d1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:52 GMT
ADD file:08addf73dde8bf5ac64e0d9bdd1997ce5f406976c19da431616783c14fdb36ac in / 
# Wed, 11 Jan 2023 02:57:52 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:33:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:34:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Wed, 11 Jan 2023 13:34:43 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 13:34:43 GMT
ENV LANG=C.UTF-8
# Thu, 02 Feb 2023 22:53:24 GMT
ENV JAVA_VERSION=20-ea+34
# Thu, 02 Feb 2023 22:53:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/34/GPL/openjdk-20-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='1c8e4809d7444903dfde02ef45821c1206a5d98c241c04280434ef9b5aca15ad'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/34/GPL/openjdk-20-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='6e43b2f39d2b6359755a6cd26c01057b1b6d53c84d944fc3396500b2f21a15be'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Feb 2023 22:53:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7fac02f4cd2bcf681b9e156a67009cf4609f45447818b52327d93553bfeb2965`  
		Last Modified: Wed, 11 Jan 2023 03:01:58 GMT  
		Size: 25.9 MB (25914925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c3b6f956b3fce7c340f2d003d19d58e27ae60d033838d462212b60d5e10443`  
		Last Modified: Wed, 11 Jan 2023 13:40:37 GMT  
		Size: 3.1 MB (3129360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803ec72066ab4c64a3b9aa900bd1cc56b71d832097af024d274588777a63ccf2`  
		Last Modified: Thu, 02 Feb 2023 23:03:27 GMT  
		Size: 197.0 MB (197013397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
