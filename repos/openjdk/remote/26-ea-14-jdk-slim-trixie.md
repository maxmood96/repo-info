## `openjdk:26-ea-14-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:657d9ac91c901a838be57ba30e945107a35dd01b677a145a94927878a5617389
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-14-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:9e35ee7487712a908a12db032ad6f0d864d3b358216d959c5a00772d914d3c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255600065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae7455290bc2c6b9e571282b2b8748c0fe6839ccbb3d5fbbcd13bc556feb02e`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 06 Sep 2025 00:48:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 06 Sep 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Sep 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+14
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='14787165312e455276975549713f2f8699344989dee23e7099bafa7121b78b61'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c0b7fc80b5a73fb433db4049bb05b46ed43827c082c5bfd0b6f8883400c4d91c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d39eaec1ebd09b719512161033a50272ec739de2a57a790c3a9ad50a9834ee5`  
		Last Modified: Mon, 08 Sep 2025 22:12:04 GMT  
		Size: 2.4 MB (2371163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f1401a515b47251b055e1133c964a67b5d754146db11b136a195dfb3c146b4`  
		Last Modified: Tue, 09 Sep 2025 00:48:49 GMT  
		Size: 223.5 MB (223455407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-14-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:949bad672d97012b2bfac348387c4613cc5886cd81ef57661ffe989264f7c551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f811e68974a511d01e80d691ba25cd67c8bcb3f53c257920581a7485867b83f8`

```dockerfile
```

-	Layers:
	-	`sha256:9f32fc71168c4a24e8f1e71295397161201b9d256e4c47882ad2c71aaf555a43`  
		Last Modified: Tue, 09 Sep 2025 00:25:15 GMT  
		Size: 2.3 MB (2282504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71fe4c9a170ec509b5a76340d97d91585122711c98bdaed58967eb23a08454ec`  
		Last Modified: Tue, 09 Sep 2025 00:25:16 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-14-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6d21a90a5f0e05ecf86efc663f9ab7560cf9b9ee881a35c2dd8497e8ffd862fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253750638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e183346528a9e0c4102f76a4b43d188edfaa8915624584493c4889f6565485af`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 06 Sep 2025 00:48:13 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 06 Sep 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Sep 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 06 Sep 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+14
# Sat, 06 Sep 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='14787165312e455276975549713f2f8699344989dee23e7099bafa7121b78b61'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/14/GPL/openjdk-26-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c0b7fc80b5a73fb433db4049bb05b46ed43827c082c5bfd0b6f8883400c4d91c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Sep 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2f5d2424e7ba9e596860b9f49efe6e4e48c0c90ab1274ead88b65dcb38e8bb`  
		Last Modified: Tue, 09 Sep 2025 02:19:53 GMT  
		Size: 2.3 MB (2314330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b59a00ab2efddb662166a70cec74ea6604949757d0cbe08210d26376eb6a5b1`  
		Last Modified: Tue, 09 Sep 2025 01:43:20 GMT  
		Size: 221.3 MB (221299677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-14-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:6850568f98edb5376c5e03c16a928684e0d4c8203e19a4c4658a63fc0fd326d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096b33ea9ff369cff386d63921c8c2380a469ed8a025ed76d0ab01b162ae4b8f`

```dockerfile
```

-	Layers:
	-	`sha256:18f153c2f0913fd015b06f5eb9e04d66770183af0a65827c124462acea485284`  
		Last Modified: Tue, 09 Sep 2025 03:24:31 GMT  
		Size: 2.3 MB (2282238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633b026e39d74bd5e30cc5e86847e3cd87ac07224f16ee26bd9a025ca3b0837e`  
		Last Modified: Tue, 09 Sep 2025 03:24:31 GMT  
		Size: 19.6 KB (19627 bytes)  
		MIME: application/vnd.in-toto+json
