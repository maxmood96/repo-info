## `openjdk:26-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:4fb8c6649121d9b71d114140fe57d5e5f691bdc245354d0f3f44279c788a7453
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:f58cbedfaf39e55a931ccfb2bec68381fe6851317abfa7fba62c256d04a56854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.8 MB (381789880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48feabd80722b630553bf407fc91b9148389ed9e8a184de1cb63a759015bd05`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:03:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:03:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 16 Dec 2025 00:03:32 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:03:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:03:32 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:03:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='a18910b0bdceb12a4f78147a1feebee50cc621ad8114c07a1ab071e58c17b09d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='d330a706e3fc611f4b39f6768f104e47d0a755ffabda31e3299dbc2e791f4f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:03:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c237534654fe7a5c118fcee78652af952e57a4a07cc322c0ae3c367839bb0ccc`  
		Last Modified: Tue, 09 Dec 2025 00:06:16 GMT  
		Size: 64.4 MB (64396522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c75a27385e8f29cb290dd7d161f91d27988a7bbd2b3b46e097413775c16da9f`  
		Last Modified: Tue, 16 Dec 2025 00:04:09 GMT  
		Size: 16.9 MB (16944784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f20b77b168732675708bfefdb5253d308bb3100df555a6b77eadf21109f739`  
		Last Modified: Tue, 16 Dec 2025 00:04:25 GMT  
		Size: 227.9 MB (227938503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2b2083411519456dbf09dd9337d81b5d9b726de127cac4d54ee3c6c990957521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e86708df556e6eb38257abc399ec3bc2f7e2e7a6a6956171567cfd56cac84cf`

```dockerfile
```

-	Layers:
	-	`sha256:1d663d4e1f456df9b846e367a4c7f693b793965c6e54547b18d381491c25566f`  
		Last Modified: Tue, 16 Dec 2025 01:23:36 GMT  
		Size: 8.7 MB (8668236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18bffa0381fbe4261ad557e159fe2f33bd609fd827a463c64e81ab8f8e1d94cd`  
		Last Modified: Tue, 16 Dec 2025 01:23:39 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:895c9f024f4dec69600d36f5b6cce6e3d113acba21bb82cbd1450a15afcc3804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.9 MB (379908109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa39f19c17613b12ec6ff4f1dd3ee2675d0b8a6ad1e95160d7608b9b13cf44a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:03:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:03:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 16 Dec 2025 00:03:48 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:03:48 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:03:48 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:03:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='a18910b0bdceb12a4f78147a1feebee50cc621ad8114c07a1ab071e58c17b09d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='d330a706e3fc611f4b39f6768f104e47d0a755ffabda31e3299dbc2e791f4f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:03:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a266a3916e0f2e8ff6996b219222479419b3dca87b3e3dfc3bd0108f509071`  
		Last Modified: Tue, 09 Dec 2025 00:11:40 GMT  
		Size: 64.4 MB (64371489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2487e675900cbde25dead9f939f627e659aaf934a6528ade2f30ab91ad8002a`  
		Last Modified: Tue, 16 Dec 2025 00:04:32 GMT  
		Size: 17.7 MB (17728576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda269c57a83bca85e5c13457fee30361a24c7c39ed453cda24bbdc2dd028d32`  
		Last Modified: Tue, 16 Dec 2025 00:04:44 GMT  
		Size: 225.9 MB (225850726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a78a7f3e46fc0f30fdb14c6f61b8212a4f99742ac72e02e5b07b7237725bccd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d73d4935b1c931a7a2c84207970b77b849ae644ee8067c3ba067e781d035f7`

```dockerfile
```

-	Layers:
	-	`sha256:10d3ffd957d30e6e03b2cd2cdd1f97c4ed916fbb387a9a1d371f52c5e7223f07`  
		Last Modified: Tue, 16 Dec 2025 01:23:47 GMT  
		Size: 8.8 MB (8805081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74ba6be3f04837c1be7049e2c8881ea18719091628ccbefbf7b597107696de58`  
		Last Modified: Tue, 16 Dec 2025 01:23:48 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
