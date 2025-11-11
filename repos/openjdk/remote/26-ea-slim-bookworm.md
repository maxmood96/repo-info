## `openjdk:26-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:09da7eb3cc8d9deec82ea554c451c81c4c9d1b85c37ac4aa2c67cc57c95b9739
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:a1a8243bb247e6276f542932b5d26ce1a693ab495e148dc688ec326561576cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258257384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79dd5b3b70dda145b7578f6ab2bab462bf94446c73cd8e7d94e4967af16d9e8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Mon, 10 Nov 2025 19:53:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:53:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 10 Nov 2025 19:53:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:53:13 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 19:53:13 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:53:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='c5cb587a920ddf65225352cf2494965786acd1de8d6748a976d7498d0783a396'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='427f53a6635347b853f695324253b6d78f69cc09334a9cb1031a801e43358883'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 10 Nov 2025 19:53:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2577702809a17b65649317ed0d8d87f1c2bfe8d9bc0afdab89aab358e04accb2`  
		Last Modified: Mon, 10 Nov 2025 19:53:45 GMT  
		Size: 4.0 MB (4027353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a818916335d9823bacddc500621a4c10b89bb9cf61e5ef72c77893924699f75`  
		Last Modified: Mon, 10 Nov 2025 22:30:11 GMT  
		Size: 226.0 MB (226001464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:1eebccff49aeb54bbb0279a9e1873a541e2659ce77ab09297554b3baa0296272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4a9139835e4a104fec412346028c208f8f569754fd866ecf15d81d274af227`

```dockerfile
```

-	Layers:
	-	`sha256:a9321b1db0d5275eb485eb3a1f0f84fab84f554ae1b16ff20742065a43b78575`  
		Last Modified: Mon, 10 Nov 2025 22:24:15 GMT  
		Size: 2.6 MB (2649789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a322f06c7f79308152558805673c8287ab791ebccc50424a628f3ca550e2056e`  
		Last Modified: Mon, 10 Nov 2025 22:24:16 GMT  
		Size: 16.9 KB (16870 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:25baf8facc0181c01133541d20a001f95c704dc06a291cc3d961241ab94f1601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255811744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860f3c40b500404823b53563cc28e8fd828058e00dafbda89f6ac01bcb087765`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Mon, 10 Nov 2025 19:52:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:53:04 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 10 Nov 2025 19:53:04 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:53:04 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 19:53:04 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:53:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='c5cb587a920ddf65225352cf2494965786acd1de8d6748a976d7498d0783a396'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='427f53a6635347b853f695324253b6d78f69cc09334a9cb1031a801e43358883'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 10 Nov 2025 19:53:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68aa11b19a6317cbc8f8062ea288304e5e33249713e3ed1c5da8a029e0903159`  
		Last Modified: Mon, 10 Nov 2025 19:53:36 GMT  
		Size: 3.9 MB (3851327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2acb22538f0af46cddd4f2dce0ad40cf43464201c3731f9195e467170bd0a91`  
		Last Modified: Mon, 10 Nov 2025 22:26:08 GMT  
		Size: 223.9 MB (223858041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d564784eb3636075543cfd15793354bc61cf3ae752d75ac8ef413c399204c450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fad570efae170a1904acbe4f1fc374d3f1547e6e65dbaa621982e01be773e1e`

```dockerfile
```

-	Layers:
	-	`sha256:9057cda3689a05100f276e7af3979d7b8ac09a84306ffdcff0d4caf974798166`  
		Last Modified: Mon, 10 Nov 2025 22:24:20 GMT  
		Size: 2.6 MB (2649423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8526768eb39acdab0f38e1de368c0372ed839496c445f5d61781158420d32ec4`  
		Last Modified: Mon, 10 Nov 2025 22:24:21 GMT  
		Size: 17.0 KB (16989 bytes)  
		MIME: application/vnd.in-toto+json
