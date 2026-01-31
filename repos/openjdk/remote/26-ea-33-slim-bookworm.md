## `openjdk:26-ea-33-slim-bookworm`

```console
$ docker pull openjdk@sha256:dd83b9a01445b05e959c3a40b2b05cb0e1f476021651890670f6d245757e34ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-33-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d38dae2dedf738a7df06c9d1211681c22ca8c55dc00b5fe695fd9d29b195e6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260293379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4bf66f4d76adc81c7c4e492777096be6353b006c85ca8670c082fae6651903`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 30 Jan 2026 23:39:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:39:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 30 Jan 2026 23:39:52 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:39:52 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:39:52 GMT
ENV JAVA_VERSION=26-ea+33
# Fri, 30 Jan 2026 23:39:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:39:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1570c898956f12881af49a97b3381e1155aa730fd222401c81712bf6758db662`  
		Last Modified: Fri, 30 Jan 2026 23:40:12 GMT  
		Size: 4.0 MB (4029225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3cb2bd0eb6af803c9794ffc5146317002feb6782046878540fb50dce801391`  
		Last Modified: Fri, 30 Jan 2026 23:40:17 GMT  
		Size: 228.0 MB (228035582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ef3007a29b18b732812611058bf7c1ec4d7dcf38a24760fbac5f19a5254c6bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d0745ee533c1967775bcb032302f5762bdcada94ce7cbdaf2264f28f500b4e`

```dockerfile
```

-	Layers:
	-	`sha256:7c2749098527042ef60d97bd5deb9fa4d448b6c13fc3a141683d78dd2cf0bd96`  
		Last Modified: Fri, 30 Jan 2026 23:40:12 GMT  
		Size: 2.6 MB (2649799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e5dd7bef95c7f85f012cfba87ddffe040bacc2220c39c6facbcb8aa7eb82117`  
		Last Modified: Fri, 30 Jan 2026 23:40:11 GMT  
		Size: 16.9 KB (16870 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-33-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c1dd985e607b5ee80ed013f37569391f8ebddb8882ad9a8b893e251d50a7b403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257907774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd0f773bcb946bd4cd1fd874581295c26fb30a2572b1a150a84a641e3f0d3a0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 30 Jan 2026 23:39:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 30 Jan 2026 23:40:14 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:14 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:14 GMT
ENV JAVA_VERSION=26-ea+33
# Fri, 30 Jan 2026 23:40:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd65037ca87c325a0615cd82fee95c786d4deba85fa7c97709878baf025d4a68`  
		Last Modified: Fri, 30 Jan 2026 23:40:35 GMT  
		Size: 3.9 MB (3851956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bdd774913dd4004d4bbc2ff2e8377897ebd4a6a122a812c4368e70f75ae88f`  
		Last Modified: Fri, 30 Jan 2026 23:40:39 GMT  
		Size: 225.9 MB (225947929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a27408eae93370b71ace9b751fbda668ab4130086d4f04ee85781c9dcb379926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c720787f08ab96c299378126739e0077d126be71fa2118c6c142f6ae142f7140`

```dockerfile
```

-	Layers:
	-	`sha256:e3ccb14277c51b274fa4ba71a53fe37491fa612466aae0d8a5b5f0f410945001`  
		Last Modified: Fri, 30 Jan 2026 23:40:35 GMT  
		Size: 2.6 MB (2649433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd1b872d7ade0b0a58ec29b3cbbb1de3e8762335c7c10d3b623497b5ef672633`  
		Last Modified: Fri, 30 Jan 2026 23:40:35 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
