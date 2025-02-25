## `openjdk:25-ea-bookworm`

```console
$ docker pull openjdk@sha256:d90eec7a5c9d79a7b5935d9c02bd0f10b2d0743937a51e2ab48d3446a264da3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:0c5fe7d153f01739fc8e16d16e84036438f0122f1f2dd00d2748b711b8b3ecd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.8 MB (365806354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec29e41b810ac70b1ac16cd7e3c8b400539795d37f25e0ac0448f4d73c8012aa`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 21 Feb 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Feb 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+11
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='48a39baf57099268625cdafd903613bf54229d97dfd800d01733e036770a89f7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbbf2112e28aede77dc8f42dd8e27e6bcdd34cb862b5dfbb3b1c15c709fedf19'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf243abd1843f2d8e25d28ba482e158109e0269d01c329fc1beb59a06ad0099`  
		Last Modified: Tue, 25 Feb 2025 04:17:52 GMT  
		Size: 16.9 MB (16943086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f1bec673cd225cf56e348243bd72199a9ef2a8fd3e7ced40d9890305c7e173`  
		Last Modified: Tue, 25 Feb 2025 04:17:56 GMT  
		Size: 211.9 MB (211934423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:1814eec9064b690b0937e670f90cf1a210ad8908daf2e61048c19a28d40b2403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8458019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153af6aae58b71e963242d4bc869295b311a2dabe4ce69456b72ca9d3bf842bb`

```dockerfile
```

-	Layers:
	-	`sha256:bb5cee8ac1c2fccb7325863a2ddab3323e856516af5dbac9cfa035ddbdc844ad`  
		Last Modified: Tue, 25 Feb 2025 04:17:51 GMT  
		Size: 8.4 MB (8439401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6cfe84680b8e89629d4360decc2e90619b6d9d94931e2419b4e72fa9c3d9e2b`  
		Last Modified: Tue, 25 Feb 2025 04:17:51 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7ce03813b47da911c74cba4b627e5396854ca9e47ca721f53ac27d6177a6e7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363878186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b5cb6fb3dc89b293f1e944d782ee84eb1831ec0f78c34aa5127658099a1c1d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 21 Feb 2025 01:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Feb 2025 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 21 Feb 2025 01:48:17 GMT
ENV JAVA_VERSION=25-ea+11
# Fri, 21 Feb 2025 01:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='48a39baf57099268625cdafd903613bf54229d97dfd800d01733e036770a89f7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/11/GPL/openjdk-25-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbbf2112e28aede77dc8f42dd8e27e6bcdd34cb862b5dfbb3b1c15c709fedf19'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Feb 2025 01:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Tue, 04 Feb 2025 09:00:06 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d3572a68af0b860060b7ea84adfa8406fa20cfd1337c947dfb661aa965eee7`  
		Last Modified: Tue, 04 Feb 2025 19:01:50 GMT  
		Size: 64.4 MB (64357505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67f15c6066247c5954087e18794060d84d9a3a4d17a01ccfd724f83a823d824`  
		Last Modified: Wed, 05 Feb 2025 02:54:07 GMT  
		Size: 17.7 MB (17727283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56220a92a48d23b62fd25c8c14218cff9c85e7a4ea6f18c7e2eab40d0a6f7427`  
		Last Modified: Sat, 22 Feb 2025 02:36:26 GMT  
		Size: 209.9 MB (209888417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:dfbe56e6542bfab2eadd65f8191814bc4326fa0a0f3ee772bf54d44ee166d9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8595012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3baf203abb3ed1ea23745e3a775301506e345781688206ef1b80b9bc7ba8a180`

```dockerfile
```

-	Layers:
	-	`sha256:6673d3d23fc1e5e5a4f3752095879e51cd9d8f1a7f23ac1758ae2b7db40b636e`  
		Last Modified: Sat, 22 Feb 2025 02:36:22 GMT  
		Size: 8.6 MB (8576251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57fbb6e46f3ffcda00bd3d55d9b7100161aca040249e5833103314d038270b49`  
		Last Modified: Sat, 22 Feb 2025 02:36:21 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
