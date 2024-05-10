## `openjdk:23-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:29e6f225e40938281d48d50050a56a3fbb2e4e7cb1aa012dd89aaeec162ed268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:de9d9f25e66dba8f1a58f3a118fcaf319114ec104dcfec5404b9a5d7c146726f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243045923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049282ceff9c64d040db209ca59b71a035ce5915acc704750e0a93542a3d4f22`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 09 May 2024 18:48:15 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 18:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_VERSION=23-ea+22
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ccc93940dc68c8a0c9bc01591e72321cd694bfb7c70384ed377f0a615cac323b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9dd3ec5e765c2eaabfc53e02589d00865053269474c8b2c939d8ce00e5f9ad15'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 09 May 2024 18:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e832f7fd56e1dab4899e0321799d4461d346d41b277e34594710ebb7985ca57`  
		Last Modified: Fri, 10 May 2024 00:51:49 GMT  
		Size: 3.8 MB (3821779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8f0eddca5eabce33e1a4ab2fd4dc4be889981594b0c44d16adde3aa808c220`  
		Last Modified: Fri, 10 May 2024 00:51:53 GMT  
		Size: 210.1 MB (210073665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ff450c433550056472c07b267af0920f238c47bf96c40dd80a262acede77d2e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff5a270789df2274ffdd6d9eeba868622d5129f0c3e65d31e1832bcb5a58372`

```dockerfile
```

-	Layers:
	-	`sha256:bea6ba78fbf0f913daafd72322f4fef73107bbf56d2f4e5cec19e11c23cc7034`  
		Last Modified: Fri, 10 May 2024 00:51:49 GMT  
		Size: 2.3 MB (2346317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9afe0d15729e809771143fd9b25cdba21430218d5273d34cf4e99303c60b941`  
		Last Modified: Fri, 10 May 2024 00:51:49 GMT  
		Size: 19.3 KB (19348 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1e418ad447b04a4d197d13abd7fc95b4073d0fa390747ad3ad51127cd7a92c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240770497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03cb62ac8775d07bd3e7300b730a5957ef22fd89c21529e7c58d43d622e54ce5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 09 May 2024 18:48:15 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 May 2024 18:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 09 May 2024 18:48:15 GMT
ENV JAVA_VERSION=23-ea+22
# Thu, 09 May 2024 18:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ccc93940dc68c8a0c9bc01591e72321cd694bfb7c70384ed377f0a615cac323b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/22/GPL/openjdk-23-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9dd3ec5e765c2eaabfc53e02589d00865053269474c8b2c939d8ce00e5f9ad15'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 09 May 2024 18:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2231cd3e935484a1d6bb796d839bb9808c1ebfa58930675c64dcda3530e5d490`  
		Last Modified: Mon, 06 May 2024 23:50:25 GMT  
		Size: 3.6 MB (3629765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6883e3c4ad29830c0dfd570659d790500c1ad27bff7eac66c55c9d4ccfc4a4`  
		Last Modified: Fri, 10 May 2024 01:16:24 GMT  
		Size: 208.0 MB (207960797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e3f6c9402861f2cb40cf81ca34380cd6e0882aa03cdbc92a02670426e54281cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e648961c85a62a3a6ea6be6c2101ecbde95b33b83fcc611a45502e83ce763a`

```dockerfile
```

-	Layers:
	-	`sha256:b758ead2a1fd82c0e04fe652785c43e8efddfca998d4aee7bb2d53922aed932d`  
		Last Modified: Fri, 10 May 2024 01:16:19 GMT  
		Size: 2.3 MB (2346546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42254077d5005ed989bc615f0a08cf1071b0705d9a1f681a4fe97a6aaaa7720`  
		Last Modified: Fri, 10 May 2024 01:16:19 GMT  
		Size: 19.2 KB (19207 bytes)  
		MIME: application/vnd.in-toto+json
