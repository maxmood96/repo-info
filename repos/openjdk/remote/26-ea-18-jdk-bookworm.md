## `openjdk:26-ea-18-jdk-bookworm`

```console
$ docker pull openjdk@sha256:865de55805e1efb324aeb03c50297b8319931d56a23f413c69da823f00b08134
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:26-ea-18-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:0146f1fd8bebf7acb15c846c85b9f316fb2d77108c77c90bd87fa397dc60ae27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 MB (379628728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9b77a021eebf23a7a4a53e5f76722ec7edcf09d4a19271588cfef191cee0ef`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 04 Oct 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+18
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='efaa7c08b216ca30d5769c56a81337742b795188f8ab45532f711cd0fedd7971'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='2176c4bff69a4a7825dbbd296ac2ab318460f5dfe104d5590be6f3f470d7dd5c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
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
	-	`sha256:a9dc770b7b4289b5b5f08ef2e589de684a6e8e695a4db23617bf68e9a4889528`  
		Last Modified: Mon, 06 Oct 2025 21:06:04 GMT  
		Size: 16.9 MB (16943577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e7f23e848f940058091c33c18ab00a42a907bcecd41e87ac970983368fa30a`  
		Last Modified: Mon, 06 Oct 2025 21:24:36 GMT  
		Size: 225.8 MB (225781307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-18-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ef82582f50eab7ecfa4c246b7d9c7dc703a22905bf2cf965122b7826c0637404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8689956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7e7bd55dc0745e6793b099b0d382725fa8d73e9281a0282ad249caf4089fb9`

```dockerfile
```

-	Layers:
	-	`sha256:4b7777723e4268ce8deacb606783e28e5f13396c08726e7f8cd608ff28f60406`  
		Last Modified: Mon, 06 Oct 2025 21:23:28 GMT  
		Size: 8.7 MB (8671339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:752251ad3f06848082f9fb6e0320a0cd3e2bce27b000caf41f2606199d3c6d4e`  
		Last Modified: Mon, 06 Oct 2025 21:23:29 GMT  
		Size: 18.6 KB (18617 bytes)  
		MIME: application/vnd.in-toto+json
