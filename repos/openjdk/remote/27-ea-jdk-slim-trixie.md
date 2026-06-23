## `openjdk:27-ea-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:9a5913201bef29674fe991726fdeba2db5c562a57fb7b939bfb87b4a7dffab1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:602c04c23aae584e149ef2175f9b5a69a951269466312c92ab7c5e4159ab2531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.3 MB (259273905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fe55d4044beead8964a06ac8ad9666e60f5d822866b0e2b18782172f0fbf20`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Mon, 22 Jun 2026 22:37:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:37:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 22 Jun 2026 22:37:58 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:37:58 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:37:58 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:37:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:37:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff12182814e6d2de279217255abeee7a47491449756042c759af19d97baf50c`  
		Last Modified: Mon, 22 Jun 2026 22:38:18 GMT  
		Size: 2.4 MB (2371340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cff3784c91550f755cea920d3e8e1500e2a35d9ebb4e977bfe995c71a8c26e`  
		Last Modified: Mon, 22 Jun 2026 22:38:24 GMT  
		Size: 227.1 MB (227117150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:8f8cb05df9d791be1e3a10bf931f201092a7940f4f0cdf29e4420bbc0c8f5a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be82d531fdb7a4c6b06957fb75c66a17d97818951a5552de1ca2bc6f0fa8cae`

```dockerfile
```

-	Layers:
	-	`sha256:9c833b262f1ad03802e3f5dbc7dbcfb92c36728f40586d883387f6aaec7cda2c`  
		Last Modified: Mon, 22 Jun 2026 22:38:18 GMT  
		Size: 2.3 MB (2276384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:610db3621a417a4af5482f81e8074736b6303542b6d6594ec1ac7fd8ac51d689`  
		Last Modified: Mon, 22 Jun 2026 22:38:18 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e13f219ed4413bcce974fc1fa39b1734239fa395d87307b1a2996a044ecb684d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257563809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6450f1b117f28b44681d07a0fd95006e65ec8fff6ee259cd3d136b3ec833877`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Mon, 22 Jun 2026 22:37:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:37:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 22 Jun 2026 22:37:57 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:37:57 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:37:57 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:37:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:37:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3294bd2806b6a084dedfc7543175da01aa12f505888c741a8e242501827a678e`  
		Last Modified: Mon, 22 Jun 2026 22:38:19 GMT  
		Size: 2.3 MB (2314590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0b4c9894c62793a4d71ba985e9626a3f61bbcc66c51a7d2a060b7bca933009`  
		Last Modified: Mon, 22 Jun 2026 22:38:26 GMT  
		Size: 225.1 MB (225100689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:3687065a9f148a0c94d02e490f7462c9a0ce0f8e4b20bbda4c42cea494b08166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada4b822834f872741bae167dc58c5d53f95345656f40a6fcdafd19f68bca838`

```dockerfile
```

-	Layers:
	-	`sha256:062580f1db8d62bb5e59720133e8f4759722444c02fcb36f748f7dfc7e3fb6e7`  
		Last Modified: Mon, 22 Jun 2026 22:38:18 GMT  
		Size: 2.3 MB (2276062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65316ab366428ee1955b53869862d6f0aec9fbe435f5b671729c920d8647638f`  
		Last Modified: Mon, 22 Jun 2026 22:38:18 GMT  
		Size: 18.3 KB (18275 bytes)  
		MIME: application/vnd.in-toto+json
