## `openjdk:26-ea-bookworm`

```console
$ docker pull openjdk@sha256:2a1170ee6c1ae6e11a2f73da9a79f0c9b032999a433f922c8b15835af84373f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d67b8d815dbbfa703d826eeaf5e8e6c9e4d0d50aa622e55e874bb8b9ce2c64ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 MB (379663111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2120bf651bca478f9b5b95f244cb52f3b19e8c7bfc0cab51cdedbdc944928bc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1b35a6fc14463ada297f3f0605409cbfe29368b38fd5d1e41f7dcf29bb6fb`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 64.4 MB (64397411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c54fa53c4f5b21a648b29e747f284bb16595f62b65e4e7ebab8f8b4cd36f739`  
		Last Modified: Mon, 13 Oct 2025 21:03:09 GMT  
		Size: 16.9 MB (16943653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b9043d2e65778baa53d2d2ad593e9c6931519e969465ba477166fdcad87311`  
		Last Modified: Mon, 13 Oct 2025 21:03:02 GMT  
		Size: 225.8 MB (225815614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a6a6cfcbe694dffdc04ed5974475bcef69f9e394db8209ce8ae8d94d27e9d3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8689957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4341edaeebd23acb24a75ccf0a496d28406866a5f0a4b5d22439622de5c08671`

```dockerfile
```

-	Layers:
	-	`sha256:cec331a25aa8c306aeef7dffd1f99f84d7c7ead27574bd977f6bcaf5455e2533`  
		Last Modified: Mon, 13 Oct 2025 21:23:34 GMT  
		Size: 8.7 MB (8671339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a106b55f762970472de935947fd46ff3944683b1e6682b8701aeb5d3f948b6ee`  
		Last Modified: Mon, 13 Oct 2025 21:23:35 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b766903099740b803bd440eb79c845cbd092075a279222a77307560a50227363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.7 MB (377725379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3f5f1d598dcd971e6474075580d2a0d61aca62c94e9a011a49b73639574eeb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2f93f2f0e198bff671333b38213c36ed741b7f552b83c033cf63f52b58c0e`  
		Last Modified: Tue, 30 Sep 2025 01:19:31 GMT  
		Size: 64.4 MB (64371209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c8264a16aa7a7b627d4f36db2280c73ed5ab988fadc3c23a65e2ac91bae4b6`  
		Last Modified: Mon, 13 Oct 2025 18:23:25 GMT  
		Size: 17.7 MB (17727724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1c35822a30a9a9785ddb3f6371759d463068aab410fd404cac341a30c7423b`  
		Last Modified: Mon, 13 Oct 2025 18:23:18 GMT  
		Size: 223.7 MB (223672797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:232fec45b3e40094975b6796cb2e984888a15e0c19df30e11753b2e80cecf6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8826969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d3011b4802b44c60c1beff156e4e3175620994c29ef64a782132042b3b828b`

```dockerfile
```

-	Layers:
	-	`sha256:8095bd09b102b5688893c67d1a5c691d378f0846b2e9fdb825513c6a91d288ff`  
		Last Modified: Mon, 13 Oct 2025 21:23:41 GMT  
		Size: 8.8 MB (8808208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ecace43ddde487878ac0947a481bf63b36c213a51b0ac648197b5de0f75f6d8`  
		Last Modified: Mon, 13 Oct 2025 21:23:42 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
