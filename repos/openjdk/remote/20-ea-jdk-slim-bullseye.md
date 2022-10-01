## `openjdk:20-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:987099876cf4bb86435e98dc7e3be04e12c6c6b296e39498e190ac1a8e76fe55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:22c268d0cf12f447f5afcff21553d18ee42b8f33d4e83c43b44ff3aa575c2db4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230262341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcefe233dbdea8e70fe53eb85e652c6d770508b6894272ce58003776c05cc306`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 07:01:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 07:01:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 13 Sep 2022 07:01:59 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 07:01:59 GMT
ENV LANG=C.UTF-8
# Fri, 30 Sep 2022 23:30:48 GMT
ENV JAVA_VERSION=20-ea+17
# Fri, 30 Sep 2022 23:31:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9d46acb0892a134f62ab21fca33fdef1da5d579f61ddbd0ae3ff0b4d33c5eca2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='31245b15195bf9f12a6db08474bfcbd1ddbccc76436372bf4db538c6ede8f976'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 30 Sep 2022 23:31:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e69b53e7b682e7dd85bc12ebde7a4734ebd6cf1c24c9932ed6d0f5ad309612`  
		Last Modified: Tue, 13 Sep 2022 07:09:16 GMT  
		Size: 1.6 MB (1582302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50871ce7d4c93eeb5858152b7d5cb8e4b03503f7497360a4184bc13c9868348`  
		Last Modified: Fri, 30 Sep 2022 23:36:11 GMT  
		Size: 197.3 MB (197275918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3d1d5987463297f5eacc18dcaa1fc30d3beed33b1e0a2ae7e342677462e4d09c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227244743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654b126a67636d576c018cc511c4b8ddaa60dd5f7459a3c3435d5582a10aceed`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 14:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 14:38:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 13 Sep 2022 14:38:03 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 14:38:04 GMT
ENV LANG=C.UTF-8
# Fri, 30 Sep 2022 23:28:13 GMT
ENV JAVA_VERSION=20-ea+17
# Fri, 30 Sep 2022 23:28:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9d46acb0892a134f62ab21fca33fdef1da5d579f61ddbd0ae3ff0b4d33c5eca2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='31245b15195bf9f12a6db08474bfcbd1ddbccc76436372bf4db538c6ede8f976'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 30 Sep 2022 23:28:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45dff4c2315c7ba5819fcc75c0bf4e213049019660b96d9d0fa49d7361693e85`  
		Last Modified: Tue, 13 Sep 2022 14:50:08 GMT  
		Size: 1.6 MB (1565978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270bc33f5aff9e8c8b32dc3d4b9dbd3cdbdef4547f43369143bf79435b7b1239`  
		Last Modified: Fri, 30 Sep 2022 23:36:45 GMT  
		Size: 195.6 MB (195624526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
