## `openjdk:25-slim-bullseye`

```console
$ docker pull openjdk@sha256:84f43a39150f87120c7109db27be9b054c4d59bfaf73461bbe69e7d90c4f450c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:988aed8d0fa3baac593cba1a48c1572586bbde7f3439a49def9a8cceccb375f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.4 MB (245422948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93922b9bfc2be2833d9a8e1b133dedbeb88e1e4964a17f134074732bcc0350`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 May 2025 00:48:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 16 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f2d8788017e8ffb7bf559492efe8fb46d20d613df50a5eafaed7a8344a54a5bb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f1c62c8b60be587c98a541129878b43e854c0fe167710878aa719e7f3dbefa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f9a49e2086f71740beadee7319546b25fa9f3815b11a7bb0b972cb13d41a01`  
		Last Modified: Wed, 21 May 2025 23:23:58 GMT  
		Size: 1.6 MB (1583497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4994c5fbb52f7810813517194156fdd02133de68e5d3452eef429e359e6c450a`  
		Last Modified: Wed, 21 May 2025 23:24:01 GMT  
		Size: 213.6 MB (213583511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:bd16410ea28401a0b47b76225ef1d400ac2e72fa04e91d4cdf9d14bc0b4a907d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6051c0047d491b8ba875d93599c9f78cae0c4794f157aba886a24d68a1fc86ac`

```dockerfile
```

-	Layers:
	-	`sha256:2183d97e1bcaa9e4f36f4dc90708645ca703b1f20b98614e4485594261f11dc0`  
		Last Modified: Wed, 21 May 2025 23:23:58 GMT  
		Size: 2.8 MB (2848791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e1c7e6ce02d60735ed7b485c8d476e12cd59f87a169271917184f466008ae5`  
		Last Modified: Wed, 21 May 2025 23:23:58 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e5d68f1739da960b9e4cb8a98a964f7feb7e41a0dc1b0298a8d504b5ecd95a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241669651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64832551e836dc93b267f5ac579086598899a0cf5f00a9e7edc8311608483b28`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 16 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f2d8788017e8ffb7bf559492efe8fb46d20d613df50a5eafaed7a8344a54a5bb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f1c62c8b60be587c98a541129878b43e854c0fe167710878aa719e7f3dbefa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1d03c9692493694719245e4b5b02ab0a2a3800faca912a034232dbda85c83`  
		Last Modified: Tue, 29 Apr 2025 20:31:09 GMT  
		Size: 1.6 MB (1565931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995fba350691e50c40c221118a8faf571cfd863e856994ca5796a92f100cfcce`  
		Last Modified: Fri, 16 May 2025 20:57:45 GMT  
		Size: 211.4 MB (211359075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:6033cfcddfe5f654244d7ae0433ba591f7ce67c6f31868804a6e2332411f7ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125e1096e273fc9c9b0e6373bb13edf60854a8c16b2e04fed289459b212967b9`

```dockerfile
```

-	Layers:
	-	`sha256:d2dc5295b774b004a1d53807798f57f77a955b6192dccddb059f55b7e6b299fc`  
		Last Modified: Fri, 16 May 2025 20:57:41 GMT  
		Size: 2.8 MB (2848443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a44067022c98df9a0c4024e574be5b60037dab188321422996fd6efe88c715`  
		Last Modified: Fri, 16 May 2025 20:57:40 GMT  
		Size: 17.7 KB (17712 bytes)  
		MIME: application/vnd.in-toto+json
