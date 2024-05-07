## `openjdk:23-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:4522ad40a423352cee560bef06ef63cad7b7ccb861a015723b3f37c0bd40590d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:e7f111d283eb8afcd74fbad6d9105b8e5d49022d8e0b21d199b939a71addf531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243013319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5ca22d46f564aab0bca3a94bc0f549601c12cba33b342d1c7eec521b286b7a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 03 May 2024 00:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 May 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+21
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='20f3d065d5757feeac026eba758dd431f1343b5087c7f0f03ef8bbd2fa606bd4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='33a4798e59e479514004a62ec1863207430915212696689ea072cd7ad0b5d15c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 May 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26af8f12febd104cc61a17b9f8c1ade94a94974a57c50005c09f10f91cba63c6`  
		Last Modified: Mon, 06 May 2024 23:05:48 GMT  
		Size: 3.8 MB (3821809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e7e2c931bcac4755f13207c505a4889d68812f2af638d0eb005df24418538c`  
		Last Modified: Mon, 06 May 2024 23:05:53 GMT  
		Size: 210.0 MB (210041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:86a6943a7916a6a45898102a2fe6dabc2d4c8d150e7a1227e304a610ec93e2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71383cbdc2ed7024ee228d0238b3ee355135d5d9e03302bea27dba2d76953dfc`

```dockerfile
```

-	Layers:
	-	`sha256:11559c920014a0d0dbdd05daf175a7147aa3ae98efffed38d58ee31d4ee6277d`  
		Last Modified: Mon, 06 May 2024 23:05:48 GMT  
		Size: 2.3 MB (2346317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e580070a1cbc6937cc84430bcde1738c59aa285ced310e77d78d4e72ede779b`  
		Last Modified: Mon, 06 May 2024 23:05:48 GMT  
		Size: 19.3 KB (19348 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:35bb1036edbc1fdbf0cc2e858315ed6cd33d41892b422af2e1a2dd85beafabf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.7 MB (240728727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69164557fc20912fd826ea578e04ca4630044d75e25570756f0dee69b5fd41af`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 03 May 2024 00:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 May 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+21
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='20f3d065d5757feeac026eba758dd431f1343b5087c7f0f03ef8bbd2fa606bd4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='33a4798e59e479514004a62ec1863207430915212696689ea072cd7ad0b5d15c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 May 2024 00:48:12 GMT
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
	-	`sha256:0a42eab804b94628b25ccc7ca8ab337645abc2f8f7fab5c5a2e532c351156a07`  
		Last Modified: Mon, 06 May 2024 23:50:29 GMT  
		Size: 207.9 MB (207919027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:de216b76e2bc8691d643232047ce3bb7b3e4b8c2276408a62b6ff7a0cdb58cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2454215b2fe3ef9fa8d780743e78a639f938061f8ed7abd2b71b7a1c564088`

```dockerfile
```

-	Layers:
	-	`sha256:d087ee5b078349cfdd04ce3ff4582ea19bc8b4377548b06da56497adb7f32993`  
		Last Modified: Mon, 06 May 2024 23:50:25 GMT  
		Size: 2.3 MB (2346546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1bbcec18b29607a57f4c4212f845bedabb2d41596004110ef53b12f4ce17076`  
		Last Modified: Mon, 06 May 2024 23:50:25 GMT  
		Size: 19.2 KB (19207 bytes)  
		MIME: application/vnd.in-toto+json
