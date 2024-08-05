## `openjdk:23-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:4a268706b8039ab7af954b023850068cf92ca3e8fdfbd664be76c137d35c3342
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:bf0258a090c1a71e1b09954a6463894ec5385dcb9067cd7b5772b54517abc521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244623388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51290d72965c5d49658a68b796720539a048de1c1ed646c0fa920d3ad2506acb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:15 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Tue, 23 Jul 2024 05:24:16 GMT
CMD ["bash"]
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 02 Aug 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+35
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='5387c8da8acb4261265c12bb46cea856c248d70bf9d64164019b74ed96545655'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='d5765b057a4eca4913ddd3d661e0ecd9cb182d4ad79359a645e427bdadd574d1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4502e49a4f58f62bbf08cb540164b398de668d3e12bb3992079348be9822bf`  
		Last Modified: Mon, 05 Aug 2024 18:57:49 GMT  
		Size: 4.0 MB (4016754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74203e9def0d8ec15e5393959b9d5d0080db9ace85b03077080a22fdbc49806f`  
		Last Modified: Mon, 05 Aug 2024 18:57:52 GMT  
		Size: 211.5 MB (211480347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:222418e6c8d02c5aff44b4cb8a3046f39b1069581c243d958ed5f767a320ea47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f092ed5de165dc676a069b1630ece4790d14d7b7cde47bfe52112d6124cff9a`

```dockerfile
```

-	Layers:
	-	`sha256:e83f4b5485a7948e1c8308da0fe9e08680c2fe17886010de9a98d2e988edd69a`  
		Last Modified: Mon, 05 Aug 2024 18:57:49 GMT  
		Size: 2.4 MB (2365306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a13c9036a3f36420fb066f16ef673fed5087938c3db204ececed621b0b7c69`  
		Last Modified: Mon, 05 Aug 2024 18:57:49 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e6875755b17d78987f5bda0d15a278ecc938519c7f0f9572604fc40018970715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242334274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13336e653433ea8867fddabb4dc3c4af6179e026e32bdd9393f2deb2aafb9cdc`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 02 Aug 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+35
# Fri, 02 Aug 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='5387c8da8acb4261265c12bb46cea856c248d70bf9d64164019b74ed96545655'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/35/GPL/openjdk-23-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='d5765b057a4eca4913ddd3d661e0ecd9cb182d4ad79359a645e427bdadd574d1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c349375e2e294f7eff4dd86f726854408dbf40098a96b9250ed96a5be15a73f5`  
		Last Modified: Mon, 29 Jul 2024 16:59:58 GMT  
		Size: 3.8 MB (3829955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8147e54558d3ce22bfb22dbe766a6237c31ceaa1eb3bd1390ccac43638b2e895`  
		Last Modified: Mon, 05 Aug 2024 19:14:26 GMT  
		Size: 209.3 MB (209347748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d519fc7c151251c26240e9a717da9336a6166cadc794a30bbc892f8571861953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae081951ea4d885b61962eea54416c6bdb4c018e6a70177d6452aa0706a03851`

```dockerfile
```

-	Layers:
	-	`sha256:3abfef620b08c6a4dca0649cc7a1a5a96b4523d42adf489e3a3bef2ec27ae17e`  
		Last Modified: Mon, 05 Aug 2024 19:14:21 GMT  
		Size: 2.4 MB (2365660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:943386102a13c793b3b6e84080a9a324529f0c7fdf78fb89e3ab0a7eecc25642`  
		Last Modified: Mon, 05 Aug 2024 19:14:21 GMT  
		Size: 19.6 KB (19634 bytes)  
		MIME: application/vnd.in-toto+json
