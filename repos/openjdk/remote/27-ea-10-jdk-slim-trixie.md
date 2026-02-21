## `openjdk:27-ea-10-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:2d28860816545f5059f4c588c6972e69dfad31a528293181f97aa8ff1b61e6db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-10-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:87e51c8dbcf5e1e35391303f04853e8081a1f0bd1f4b4a8dd6dc85ed084e6a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260700628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8073a1356bf0a683ca17d3124ce48ed27661929bbfbbee8cb31559c258cb47bf`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Sat, 21 Feb 2026 01:29:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Feb 2026 01:29:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 21 Feb 2026 01:29:17 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Feb 2026 01:29:17 GMT
ENV LANG=C.UTF-8
# Sat, 21 Feb 2026 01:29:17 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:29:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 21 Feb 2026 01:29:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71661c7d9a5f636e8f1bda5542e6b433599fa4dc5da5636c201275c45babf9cb`  
		Last Modified: Sat, 21 Feb 2026 01:29:37 GMT  
		Size: 2.4 MB (2371008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9209e07c786b0ff3105ff51796b6521834492e2287fab0c3296b6dbb29ad12f7`  
		Last Modified: Sat, 21 Feb 2026 01:29:44 GMT  
		Size: 228.6 MB (228551024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-10-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d5d2194855855db21ee6c06116b042b586420b8c6fff60397492ee2085885bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51aa515f981b2e25cdafcea9fc0d6c114088334428370d9a4c7fec3e1e3109a`

```dockerfile
```

-	Layers:
	-	`sha256:e37803d6f7131d1e15eccf20b20bd91047151260049ff7fb5ede9f2ee6808115`  
		Last Modified: Sat, 21 Feb 2026 01:29:37 GMT  
		Size: 2.3 MB (2278857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf2bf819a4644c869e664cbcd00d94e52b91c45f11b7d0ca1090cebac667453`  
		Last Modified: Sat, 21 Feb 2026 01:29:36 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-10-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e0d5726878662e9bf94b1d623db8c368d88cbb151ac3b5c5f8199ae32289ae41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258958421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd0edc9fd2ec8c682efb0ac211956704f9637b66e682c111635f41cc8171dd9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Sat, 21 Feb 2026 01:28:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Feb 2026 01:29:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 21 Feb 2026 01:29:05 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Feb 2026 01:29:05 GMT
ENV LANG=C.UTF-8
# Sat, 21 Feb 2026 01:29:05 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:29:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 21 Feb 2026 01:29:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d915beea6fc42394529f5c0a0d85c0b2443b40d3593e8191b5d541bf730ab366`  
		Last Modified: Sat, 21 Feb 2026 01:29:27 GMT  
		Size: 2.3 MB (2314392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998c33a9f528898465f2a3f431f697b3085ef2e887f29ceb9d09103f84ac8d30`  
		Last Modified: Sat, 21 Feb 2026 01:29:31 GMT  
		Size: 226.5 MB (226503965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-10-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:08fb1473dd4b66a4ae3a1e628bf0e352da3693c9b815bd3bad426ea6d887c367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed964d50f2bdaf3db151c73395aea8c29285ea9e2b1f7b4e382f64a2ba73ccb7`

```dockerfile
```

-	Layers:
	-	`sha256:c0d49223ae19e29deaac798285a6af25c7abf8fd5c0019a60b0208d49fa3b458`  
		Last Modified: Sat, 21 Feb 2026 01:29:26 GMT  
		Size: 2.3 MB (2278543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:765668249cbc0b7c5fe266d9213a49d462aa2eee2405ac203e25a0f47ad4d7c4`  
		Last Modified: Sat, 21 Feb 2026 01:29:26 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
