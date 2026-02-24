## `openjdk:27-ea-10-slim-bookworm`

```console
$ docker pull openjdk@sha256:9f9369e5b59f33a900d998e61931dc80c7c78d05990cebb56380cb92ca78f637
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-10-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:e1eef2b520f5cd3b5f3881dcbd6c14490262f92ceceebade98a3e7702a25db9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260819012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1629bd35c59bda47fc6dcc022a85877521bd23d034b9c7fa48aa272f28a9b2bf`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:28:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:28:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 24 Feb 2026 19:28:18 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:28:18 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:28:18 GMT
ENV JAVA_VERSION=27-ea+10
# Tue, 24 Feb 2026 19:28:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 24 Feb 2026 19:28:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a24b63ce6840a3eb229857b2dcb00f6109f8aa970b4b7eeac5b3cfaa56cc6fe`  
		Last Modified: Tue, 24 Feb 2026 19:28:36 GMT  
		Size: 4.0 MB (4029173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38e5bcea84f19add4ef84f35ad8a1529e0a5c993f8fe02cdcc64437b4efb590`  
		Last Modified: Tue, 24 Feb 2026 19:28:40 GMT  
		Size: 228.6 MB (228553560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-10-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0d86bd60dc871a2af2b72a020be43580d4a55bfcd5020c74d82a4ad4c5285075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8197a80307c685d67f487c01873da0cfdbf541f73871bd6a6029f884cad15317`

```dockerfile
```

-	Layers:
	-	`sha256:ce20b453877e64e7b06fefa21e45c8408e5064980e82798383b548674f001f49`  
		Last Modified: Tue, 24 Feb 2026 19:28:36 GMT  
		Size: 2.6 MB (2649805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0cab05a21ed5e83457dec8800649d8b33e45bdebea32bfe76e55a91c555edeb`  
		Last Modified: Tue, 24 Feb 2026 19:28:36 GMT  
		Size: 16.9 KB (16870 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-10-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:de80a24deab9dc563ba44b0ceb766c02a01b6f81c55356bb46d17461962fb136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258471459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879f4c3fcfbca331f00fefc2518707af36a5348620d169a0d78893d362ae5ec2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:32:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:33:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 24 Feb 2026 19:33:07 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:33:07 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:33:07 GMT
ENV JAVA_VERSION=27-ea+10
# Tue, 24 Feb 2026 19:33:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 24 Feb 2026 19:33:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda0f7d1b9b9d0ebcf9a2cc93004ab40a9afd312a7ed24e4e4f9a08fe28dabb9`  
		Last Modified: Tue, 24 Feb 2026 19:33:27 GMT  
		Size: 3.9 MB (3851915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0868e7d73e94a382004b36a0a34e95a659786d84a23eed787f64d23cfe7f5de6`  
		Last Modified: Tue, 24 Feb 2026 19:33:32 GMT  
		Size: 226.5 MB (226503463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-10-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2e5c78143719d74756a894cf35546f2c091d7112475957fd858acc9c7b145af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd3ee4759f0b7b0b7086635c742d4db845a6202f00c688c06a9c4082af786c8`

```dockerfile
```

-	Layers:
	-	`sha256:16de717223cfe3ea4de2a8cb18fef7822793e8c27e8b9af3e2d458cdf752ae9d`  
		Last Modified: Tue, 24 Feb 2026 19:33:27 GMT  
		Size: 2.6 MB (2649439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01515abb5eb97e0314de35c52ad8c377fbe35ecd7cb0a74ec9056857b547b4c`  
		Last Modified: Tue, 24 Feb 2026 19:33:27 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
