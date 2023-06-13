## `openjdk:21-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:decd1751eb6788d944624d65ce0b5129c2afe34836bb14d4740a3b9d20b47970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:9f6642ea43f06b9557c19c2912f5e7d06679afa1df85216c7afd49e57e75cd36
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237194832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d796f87dc47217b20aa30642c255cff5faa980de2a26872153821a45ec4f0f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 07:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:48:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Tue, 23 May 2023 07:48:25 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 10 Jun 2023 00:28:08 GMT
ENV JAVA_VERSION=21-ea+26
# Sat, 10 Jun 2023 00:28:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/26/GPL/openjdk-21-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='16c6b09c742e73c9e092134517ecc36db2a5e44453c8b8b5374cfac1ee367a28'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/26/GPL/openjdk-21-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aa59bb222c548c18c21cb05a71854a46263a618a72ec6f2f408328689280380d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 10 Jun 2023 00:28:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72173670925a3c8ba13478bbdf18b2e895b12815a5672faa2685b09d6ed1143d`  
		Last Modified: Tue, 23 May 2023 07:50:29 GMT  
		Size: 1.6 MB (1582459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e191fafe057702285538af03bce36df2d71ee03213c5f52ef14cc335d2c31513`  
		Last Modified: Sat, 10 Jun 2023 00:31:18 GMT  
		Size: 204.2 MB (204208787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1218b33b9aeb04002af6fd0f7ddadf076bd42bebeb2f0208a5f98ad452796e2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234179635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc02239887195abd95ac688471e2cca5273aaf806eab9e8c5a9b8e4b413a131`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:40:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Tue, 13 Jun 2023 04:40:16 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 04:40:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 04:40:16 GMT
ENV JAVA_VERSION=21-ea+26
# Tue, 13 Jun 2023 04:40:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/26/GPL/openjdk-21-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='16c6b09c742e73c9e092134517ecc36db2a5e44453c8b8b5374cfac1ee367a28'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/26/GPL/openjdk-21-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aa59bb222c548c18c21cb05a71854a46263a618a72ec6f2f408328689280380d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 13 Jun 2023 04:40:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dc0b678bee14b591fc8dcf5858d219d0fce4abb02971967b35484ea1bfdd40`  
		Last Modified: Tue, 13 Jun 2023 04:42:13 GMT  
		Size: 1.6 MB (1566460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985e123ed3a1dc803a0b2d005a284f0e37898eb324de29bb312b9b9cc345d7a4`  
		Last Modified: Tue, 13 Jun 2023 04:44:26 GMT  
		Size: 202.6 MB (202550341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
