## `openjdk:22-ea-7-slim-bookworm`

```console
$ docker pull openjdk@sha256:a384b729cf47b21b6b5a7452183c856e9dcd9ff6610389a76aa0423067515b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-7-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:571552fe4b06c41959d9ca2a01b299a19fa1c4840eb29684e1237a75c09b69d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238340286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efeadf78433bfda574d22736bb36216bca1b58b31228b5b26f0584712ba8463`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:58 GMT
ADD file:bd80a4461150784e5f2f5a1faa720cc347ad3e30ee0969adbfad574c316f5aef in / 
# Tue, 04 Jul 2023 01:19:58 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 01:52:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Tue, 04 Jul 2023 01:52:41 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 01:52:41 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jul 2023 20:23:08 GMT
ENV JAVA_VERSION=22-ea+7
# Thu, 20 Jul 2023 20:23:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='8ade79d0e0e99476e603fc0d589ed815e21c875425b86a990f9273bb6f1a9f39'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='6a9b0e91b97b42e38a5d6255f6265376eab185512b2d458b1432b682e83de0aa'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 20 Jul 2023 20:23:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:faef57eae888cbe4a5613eca6741b5e48d768b83f6088858aee9a5a2834f8151`  
		Last Modified: Tue, 04 Jul 2023 01:25:03 GMT  
		Size: 29.1 MB (29124829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbdb27ec859f702c52e07508d08c6644cdff01fc5028ae06b5440b5e48d2937`  
		Last Modified: Tue, 04 Jul 2023 01:57:48 GMT  
		Size: 4.0 MB (4008037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1f17b22bae375ca435f7b1546ff533076323d20f20438dd293b3080d4546b5`  
		Last Modified: Thu, 20 Jul 2023 20:30:27 GMT  
		Size: 205.2 MB (205207420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-7-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f84134d0a794728ffc9c0fd8c393629db70b699f37020e06c9e663e029b1eb8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236487611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313b90609bb29d2516b98858c96175e6cf3441b469047b9ae3e8860ac71b21bb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:35 GMT
ADD file:71fd66666294148382f2e6a09ae5e277d4c4e9c74402ab64b693a79387b67a09 in / 
# Tue, 04 Jul 2023 01:57:36 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:26:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:26:51 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Tue, 04 Jul 2023 13:26:51 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 13:26:51 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jul 2023 20:07:21 GMT
ENV JAVA_VERSION=22-ea+7
# Thu, 20 Jul 2023 20:07:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='8ade79d0e0e99476e603fc0d589ed815e21c875425b86a990f9273bb6f1a9f39'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/7/GPL/openjdk-22-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='6a9b0e91b97b42e38a5d6255f6265376eab185512b2d458b1432b682e83de0aa'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 20 Jul 2023 20:07:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3ae0c06b4d3aa97d7e0829233dd36cea1666b87074e55fea6bd1ecae066693c7`  
		Last Modified: Tue, 04 Jul 2023 02:01:20 GMT  
		Size: 29.2 MB (29152458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160b152e2d87fa10c40e3d8ffcd0828fc336c0c9bfed0a0f293fedd4e70afdd0`  
		Last Modified: Tue, 04 Jul 2023 13:30:53 GMT  
		Size: 3.8 MB (3817545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8918484390f2e4b180884e0aed094995a71843f7f59a908d46744e30abd6e6ca`  
		Last Modified: Thu, 20 Jul 2023 20:14:32 GMT  
		Size: 203.5 MB (203517608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
