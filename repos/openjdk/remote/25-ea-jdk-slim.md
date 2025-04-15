## `openjdk:25-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:94c66f1c176e7bd7aba72081dee721317ad62b75deb3097a3b70acbc8e1c4d23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:9b0781b4d598fdcf2fc981b3470b277d026496d5e9ed41043539b3cdfd1dff0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244276727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207f3bd4954593dab3919f8ced3cc9d2d4be0f7561e467832a4ab911e29ce78d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 12 Apr 2025 00:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Apr 2025 00:48:17 GMT
ENV LANG=C.UTF-8
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_VERSION=25-ea+18
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='ee6ce5bbdd9156680b3022019f79622afcb37c06de135a7ad1a5fe893f78eb61'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='90fdbbaad39420418298d8517acadc33369d213990f99caf8cd7f86ac27d60c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138f2d40a626f429b19505fad7ea726755503d1b2f3a973e59ebc7ab044640d3`  
		Last Modified: Mon, 14 Apr 2025 22:58:51 GMT  
		Size: 4.0 MB (4018315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f62c623c98f50dbf125ba39752e49986aacec1e09a3d575c841cad0439f5b67`  
		Last Modified: Mon, 14 Apr 2025 22:58:57 GMT  
		Size: 212.0 MB (212031153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:f79bc986bc161eb78bbd03b7b5c4c79bdd66f0cd7259ac920993fa67f26d180f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace62c8eb951f0b5e39f872dae3ce12643975f4219890b5a631c57d17a00e6c3`

```dockerfile
```

-	Layers:
	-	`sha256:dd0559b98f2a51b57316e7232686194b76cd0c18efec37b9d81cd4e2b0c6f787`  
		Last Modified: Mon, 14 Apr 2025 22:58:51 GMT  
		Size: 2.5 MB (2535252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a380a75bd38c7a756ca9d742866a7a4db89bd30d895e0e547cc6175b278ddee`  
		Last Modified: Mon, 14 Apr 2025 22:58:50 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3a8cfe7fe6fe70efaf8781f6d1d598b0fc697ee2ba1c0c33ab77962a0099cc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241745997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16dc5a92c516af82bd3ceb41a0d775862371e41050374fbf021ae950564982f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 12 Apr 2025 00:48:17 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Apr 2025 00:48:17 GMT
ENV LANG=C.UTF-8
# Sat, 12 Apr 2025 00:48:17 GMT
ENV JAVA_VERSION=25-ea+18
# Sat, 12 Apr 2025 00:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='ee6ce5bbdd9156680b3022019f79622afcb37c06de135a7ad1a5fe893f78eb61'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='90fdbbaad39420418298d8517acadc33369d213990f99caf8cd7f86ac27d60c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 12 Apr 2025 00:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def4a1792f340f4e0e43ebb2cb541cdfe0533b6378c82fea5e9db4a63dc22d97`  
		Last Modified: Mon, 14 Apr 2025 23:01:57 GMT  
		Size: 3.8 MB (3833722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5399349d3a230ad87841be2422cd8cdb5ab6e72f8f5c090e2566762260ae08`  
		Last Modified: Mon, 14 Apr 2025 23:02:03 GMT  
		Size: 209.8 MB (209845955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:21c7700dbdc3a94081da7d5dd99bd4db9725fd4f34302ee11cb12ebcd33f1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481579de1c8d20cd2289093a045330a6977363e89292d22a58b340583c8cb2d1`

```dockerfile
```

-	Layers:
	-	`sha256:a21aa17c7fed3ed6977c91bfcc9cba62ccf83cc515658e7adbcbad6b1fbbb693`  
		Last Modified: Mon, 14 Apr 2025 23:01:58 GMT  
		Size: 2.5 MB (2534982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1a19049b96e0ec8863ee8140272e249a2df24736cba6cb72bdc0ebc084462c`  
		Last Modified: Mon, 14 Apr 2025 23:01:57 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
