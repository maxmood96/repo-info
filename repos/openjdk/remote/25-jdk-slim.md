## `openjdk:25-jdk-slim`

```console
$ docker pull openjdk@sha256:41120b274ca88d5159b1670b3d1c478d458332ccc11e6af79110b7a67a288981
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:29dffefa59873e810fddc31b25168ba6f9eecc5fe6279a5c41a3e15920a2cd22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245250133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5b70a79fb3430621bfc7c4481af6fbce5f7c2f99f15d0e6f78e2aab2cd50d8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 10 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+22
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ce6d616a09c8fb4391dbe165428d33b1751a228581faf829ac0610db8120ddbf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='76b4d96328978d3ba01a6970ff47dd1f368e42e94a8ba51fb3260e07230de663'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f45a6b1af68189d815041f95b73df0b545f4292a469da9ab96fd65451014a4`  
		Last Modified: Mon, 12 May 2025 19:12:39 GMT  
		Size: 4.0 MB (4018379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d502537ffaa2e7ff30fbfec7cb190e8dd6c898142c200938e10cbc1e538bd4d`  
		Last Modified: Mon, 12 May 2025 19:12:42 GMT  
		Size: 213.0 MB (213004112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:fc15b6d12971c3b7513f880a1f3847f94e945d09fcb2a1606f269780aaf62a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ec4879e1037208a3e468df784b3e67fbe9f2c85634b5c925e233b72c5a646f`

```dockerfile
```

-	Layers:
	-	`sha256:5908c919b7b12f15a5cbb85eb8d920deae87bdebcbf821e3ec83fabde8c3486b`  
		Last Modified: Mon, 12 May 2025 19:12:39 GMT  
		Size: 2.5 MB (2535252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd7ccdb8c5e293e9fdb64d538be920b9140e44bc6845d457cd016fb555435d48`  
		Last Modified: Mon, 12 May 2025 19:12:39 GMT  
		Size: 19.4 KB (19441 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:185ca1069bb3874b327227c94ba357ce8027740e9cacb5fbc04d067a2fd9136b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242715757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a17e544d8bf664cc9e63cd68b86c2406699f1b83b1a268f9a4a74d163cf14e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 10 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+22
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ce6d616a09c8fb4391dbe165428d33b1751a228581faf829ac0610db8120ddbf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='76b4d96328978d3ba01a6970ff47dd1f368e42e94a8ba51fb3260e07230de663'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba55b79ef31d50f4f2617c67f15fd3189b2a1f953d7736811f97eb36b381d3a2`  
		Last Modified: Tue, 29 Apr 2025 20:30:21 GMT  
		Size: 3.8 MB (3833814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b3ba07854652a8932ccf0d7b0d6f38d97d5ffea892e927ff768d771d0d8d8a`  
		Last Modified: Mon, 12 May 2025 19:23:38 GMT  
		Size: 210.8 MB (210815321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:8f758b01f3a1646527883c83368d0340dd9d0619db78903d005cfc463d4c56d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660c40775f90f74e0b97914e07101821f40ac154cb7ea002aebb9307de11a259`

```dockerfile
```

-	Layers:
	-	`sha256:3bd27f7c0f43a2f836fbdc3fdc4b579f0d130329232abb6ca6203e84a6e3a074`  
		Last Modified: Mon, 12 May 2025 19:23:33 GMT  
		Size: 2.5 MB (2534982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08140d79de65143b20f8cfbc485e698f5a747162950902886fffd57a78d9f097`  
		Last Modified: Mon, 12 May 2025 19:23:32 GMT  
		Size: 19.7 KB (19656 bytes)  
		MIME: application/vnd.in-toto+json
