## `openjdk:26-ea-30-slim-trixie`

```console
$ docker pull openjdk@sha256:ab91956350377d6cde1ffa0ee4ce72bf8a7b34d7de6325e5e8a51956d761e339
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-30-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:6c5adaebec1c50fa9d5973295466c10e19ad808cce415e9bc673a02f54b8d793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260159137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a934d3be5118416c0ff93bcd5aac2d4c3bb3d6030019f2b081ce6835d72ab629`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:42:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:43:04 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 13 Jan 2026 02:43:04 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:43:04 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:43:04 GMT
ENV JAVA_VERSION=26-ea+30
# Tue, 13 Jan 2026 02:43:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 13 Jan 2026 02:43:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd676c31756edfaaac725b940214c51da5381b79a5289d7baa645d6cf6e42bb`  
		Last Modified: Tue, 13 Jan 2026 02:43:25 GMT  
		Size: 2.4 MB (2371045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d663e08f2b569be02e575aa6c041cac39c195ace72ead329fe7241627a1781f`  
		Last Modified: Tue, 13 Jan 2026 02:45:16 GMT  
		Size: 228.0 MB (228014407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-30-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:4bb85d8ab7394f50429630faa4c881bb139ce0962d4d2dac3804170f99ce4bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b6716e3ad2904ffc580c5fe315bd161897cd91ada861229bf21b7b548bde68`

```dockerfile
```

-	Layers:
	-	`sha256:728d2b068ce141c01819693f417f8deea406c8d7cd14c8f96495263bcaa2bdab`  
		Last Modified: Tue, 13 Jan 2026 04:24:21 GMT  
		Size: 2.3 MB (2278851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330ab42478e477117cd1ead0977b2ffaff0b38ad6b4490915b21af76a42dc910`  
		Last Modified: Tue, 13 Jan 2026 02:43:25 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-30-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f5084e7573eab6934c3ca26a9c1499ff65de65e537d86ceb1832b86a5cb1801a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258381574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447a0cbcef94141f18ef13818e63d4d08b4d7a4a8ff40225d5529125e9a3d33a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:46:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:47:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 13 Jan 2026 02:47:01 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:47:01 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:47:01 GMT
ENV JAVA_VERSION=26-ea+30
# Tue, 13 Jan 2026 02:47:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 13 Jan 2026 02:47:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7aa79147dad9de2119b1d63806a41e74d82c519bc5d0e22b52d3ae092846f`  
		Last Modified: Tue, 13 Jan 2026 02:47:34 GMT  
		Size: 2.3 MB (2314124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a2fe6b29eb0c1de2352db9a15250168c586463b0aa4e4c438d968a1165dd1b`  
		Last Modified: Tue, 13 Jan 2026 02:47:43 GMT  
		Size: 225.9 MB (225933408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-30-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:6c358f0314201f1d629c60e3d6a654b2c6e7ae51ef3b4692e7ecc366d1a966cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2197104f178673736926ca0f639ab9319b054781e58c86862d8babfadccdc883`

```dockerfile
```

-	Layers:
	-	`sha256:f11070f377066d4bf194e652307481b7964e194f22f53ee409b3067874bc2b9e`  
		Last Modified: Tue, 13 Jan 2026 04:24:26 GMT  
		Size: 2.3 MB (2278537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ad574a06d24ea8614d913de13b80e1c52ea789438af55411a56c5f51aabc39e`  
		Last Modified: Tue, 13 Jan 2026 02:47:23 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
