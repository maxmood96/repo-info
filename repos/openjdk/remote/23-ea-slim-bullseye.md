## `openjdk:23-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:38e514978b77551f7f362d55ec96e0e4fabc0d4fd76df07ffae4ab6e4d30f38a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:68e5f16fe34a1ee3fcb6d95e6e90f16ae84b38d6333454ad39fc4d7ae4a88898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244477716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0390bdcc888be4e30a53536a7f5786cd8d305484f405176fd964e27db5d5845`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 06 Jul 2024 00:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+30
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='847f053c0a1e23b388353fdfa7c43ebe7eae98f8221e43d561a0ad3a4c486681'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef0255786108e95110839309fe5ed09fc730c0e3d78dd3d84d3f0f7e520a0d93'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b66b19d6e6bc2fb79b65f136327800c9ddc703b9e22e62b0277262a6dc95bb4`  
		Last Modified: Mon, 08 Jul 2024 20:56:53 GMT  
		Size: 1.6 MB (1581784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fc35c05854c42e257944a9f3f36e0069cc93a0bd99b665f590e5cceca3d7a8`  
		Last Modified: Mon, 08 Jul 2024 20:56:56 GMT  
		Size: 211.5 MB (211473648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:181bee592d1daf6335ccece9a5608d7178519b60c81c1f96e07d581223a2d47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24c1316ae8412563fb8b6495447f9b665edb302ae65941bd03c6ebf21fdfaf5`

```dockerfile
```

-	Layers:
	-	`sha256:a061aabe30369da69047f1a8d463791936a441fd005a7ea1d1d15e9e61ac7017`  
		Last Modified: Mon, 08 Jul 2024 20:56:53 GMT  
		Size: 2.6 MB (2638497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d1c39482dbe7af8cebcfcdd4ae7aa27130f2202467eb57e40ee0ac98867992`  
		Last Modified: Mon, 08 Jul 2024 20:56:53 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:119523e1d629df286e87bdfc42f8873af5fca834370cb39387bfdb5bc468098c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240976429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf02dedf115bb9fa3dc9473fde0db68adde007debba008e2f96c9a1a9ca1ff9e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 06 Jul 2024 00:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+30
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='847f053c0a1e23b388353fdfa7c43ebe7eae98f8221e43d561a0ad3a4c486681'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef0255786108e95110839309fe5ed09fc730c0e3d78dd3d84d3f0f7e520a0d93'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e9a242b9bfe5ce677b1999554a7f69cb8cae2f8626ed630e47ce6136878289`  
		Last Modified: Mon, 08 Jul 2024 21:02:16 GMT  
		Size: 1.6 MB (1565908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8822317bd43fe78559bc9c232b6b788f807139425419668d182c82fb131672`  
		Last Modified: Mon, 08 Jul 2024 21:07:23 GMT  
		Size: 209.3 MB (209340906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3b557b637121bfeeb96e3cc8b131bf0240b431d6d060f40bc6ba8895a570f75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2656464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2ec98dbb6d9deecff37a13d3810dfeee4b06d2413f1c9062f51d127430f7e9`

```dockerfile
```

-	Layers:
	-	`sha256:cb20676c18562f9efb823e80847f1e853322dce98e51044d76883008d714c5d9`  
		Last Modified: Mon, 08 Jul 2024 21:07:18 GMT  
		Size: 2.6 MB (2638773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b95898e863d09624f68ac05c6dec2c8770cf3d6356205af350d6253287300b`  
		Last Modified: Mon, 08 Jul 2024 21:07:18 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json
