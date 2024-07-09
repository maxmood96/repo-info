## `openjdk:24-slim-bullseye`

```console
$ docker pull openjdk@sha256:a78e58d389a1ab74bcf02f590b294ee0be40d233f6276f9afdc3badb137b9268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:875d961791331570fc096cda5f8135e4f1342c26e998557dc6f9dcfe838ba412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244551111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35394e5422b27ee41983ee71c8c515782420b1b45254ce53e36ac3d89e24f6a7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 06 Jul 2024 00:53:37 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:53:37 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_VERSION=24-ea+5
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='d5fd5e0ac45ddcd18eec430e5207bd8df7290aa292c8cd2b11a1e8d694894514'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='7d765a014b298ef58010d0fc0e0159c942ca789fcce81ac6ca12d8d149d5288d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaa016748534d2f24c46606d57b51fb8fc03cee3cf2ad992e3344ec1d09f22c`  
		Last Modified: Mon, 08 Jul 2024 20:56:56 GMT  
		Size: 1.6 MB (1581785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae2c9f949eccb24ce018f05111ac2fb7c53fdab8e1f50163491021809a44438`  
		Last Modified: Mon, 08 Jul 2024 20:57:01 GMT  
		Size: 211.5 MB (211547042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3e8254eb0f6344575378f816568b865519139c232d9a89568548db632e2bf3ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989a49e06ed9ea50704b8be7504bdd1b31535d5067505d48a42ff4dfe0685acd`

```dockerfile
```

-	Layers:
	-	`sha256:30770bf9656cbd62187974b7ec0cc34f90a54435246e8db8e054b5ed99a4f926`  
		Last Modified: Mon, 08 Jul 2024 20:56:57 GMT  
		Size: 2.6 MB (2638489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63328a24a41abec63ed1ccdcb57411059057dbefea4a3e7cb423746202a546dd`  
		Last Modified: Mon, 08 Jul 2024 20:56:56 GMT  
		Size: 17.3 KB (17345 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5d721016beaebbbe564b88343365268ab51b0ff84c7d3137353248c066708eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241059351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee749e3f52f79858ac568cf9c4491713cfffd64b48d5c8ae98ee080ba964c378`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 06 Jul 2024 00:53:37 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:53:37 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:53:37 GMT
ENV JAVA_VERSION=24-ea+5
# Sat, 06 Jul 2024 00:53:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='d5fd5e0ac45ddcd18eec430e5207bd8df7290aa292c8cd2b11a1e8d694894514'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/5/GPL/openjdk-24-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='7d765a014b298ef58010d0fc0e0159c942ca789fcce81ac6ca12d8d149d5288d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:53:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e9a242b9bfe5ce677b1999554a7f69cb8cae2f8626ed630e47ce6136878289`  
		Last Modified: Mon, 08 Jul 2024 21:02:16 GMT  
		Size: 1.6 MB (1565908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b5d1cff9890336a8ab71a40bb8a81581de4b0efb51dfce7298390d8dd144d1`  
		Last Modified: Mon, 08 Jul 2024 21:02:20 GMT  
		Size: 209.4 MB (209423828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:553ce49ebdd40d009614e529da94671f3d8a56ab310619621a69a3d21430dbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2656440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db0028971a5d8b6684dde0cab5dfe7c743078df65dddae9cd5cffeab9793c9a`

```dockerfile
```

-	Layers:
	-	`sha256:22da8b2d308c469a2b4fcafa0d63fa5de56792568d68a64c915c43b31693261d`  
		Last Modified: Mon, 08 Jul 2024 21:02:16 GMT  
		Size: 2.6 MB (2638765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d8b5f9fc0a815bebc077bdfa20b5d90a022a2cb7debf50114f657afea195610`  
		Last Modified: Mon, 08 Jul 2024 21:02:16 GMT  
		Size: 17.7 KB (17675 bytes)  
		MIME: application/vnd.in-toto+json
