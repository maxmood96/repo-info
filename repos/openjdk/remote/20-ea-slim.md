## `openjdk:20-ea-slim`

```console
$ docker pull openjdk@sha256:fed61685f82414fc1de1f4d0851d750773fae2c4ebe83aac7df6d471e78ad670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:762ee4c3f35af60cd3323f25f29e6fca4ed8553b3f9cd68ae5db0f29a2cefd68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230500473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c600603310a13c46fbfe3abb0eaebc44ba61ac8543ca93e993fa203b9390c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:28:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:28:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 25 Oct 2022 04:28:36 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 04:28:36 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 04:28:36 GMT
ENV JAVA_VERSION=20-ea+20
# Tue, 25 Oct 2022 04:28:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='0cb0f79bee2e61134a86049952a1e572bb3e2dad49aa200a20f18c697715a402'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='4db7319dfbfb4a3561e9707c0178d0ba8d6413bc94f13d8c9ce406fd7445e000'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 25 Oct 2022 04:28:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0c51c853f1ed357ae3b43810ec22a04514f065ef40f23f55eb8ab9bae73ed6`  
		Last Modified: Tue, 25 Oct 2022 04:32:27 GMT  
		Size: 1.6 MB (1584028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebbca6df7e919ba96907edda1beca04ee6ec77712d368060cd7a225e92514ef`  
		Last Modified: Tue, 25 Oct 2022 04:32:41 GMT  
		Size: 197.5 MB (197496407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e0c1e316c1e4364c2dacc2dab608bf3fe3a16ee10b1470e474f5e3f9206347d2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227684879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589e4dbc57a5e53f9ec6d7fb9e751a80c579407fd21a8b9cba2dd211c3f26d54`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 00:44:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:44:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Wed, 26 Oct 2022 00:44:55 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 00:44:55 GMT
ENV LANG=C.UTF-8
# Wed, 26 Oct 2022 00:44:55 GMT
ENV JAVA_VERSION=20-ea+20
# Wed, 26 Oct 2022 00:45:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='0cb0f79bee2e61134a86049952a1e572bb3e2dad49aa200a20f18c697715a402'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/20/GPL/openjdk-20-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='4db7319dfbfb4a3561e9707c0178d0ba8d6413bc94f13d8c9ce406fd7445e000'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 26 Oct 2022 00:45:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bdfbae33c6911a76bc185eeefca5a0dbaf0fef45662a466761c25b7448db6c`  
		Last Modified: Wed, 26 Oct 2022 00:51:43 GMT  
		Size: 1.6 MB (1567481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f82710702432dffddd90b4c5fb1b3c83c5cbc093ed23a26a773870a7f1ac946`  
		Last Modified: Wed, 26 Oct 2022 00:51:54 GMT  
		Size: 196.1 MB (196053488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
