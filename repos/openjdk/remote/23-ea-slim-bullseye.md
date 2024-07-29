## `openjdk:23-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:05edc77456f0246f4db98798d05bdcd939b3ee2d6436fdb334de31def6f3a5b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:f9de39f4b6fbd02a394707a0a016f8f3a42c882dfe2b4c1722f1b901acdefb4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244488714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141702c6aea0b1a2bb511f0a8bc6ee9e53709f41da89efd353ef0086d5730017`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jul 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+34
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='9d3fa4fbb8247f3a47788c52c09ac5c265e023cfda821610ade2a43104bdaace'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='f79a40a5860e7b57ced61d19167847390dbe4f370c7511cf7923f75d4a546363'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d342b01587a600b1532bca4b7bead72edecf8ecef9d97f8650744d9ed844c392`  
		Last Modified: Mon, 29 Jul 2024 16:56:33 GMT  
		Size: 1.6 MB (1581772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab402576c04c0fc0cb44baccda5fbcd26321af3638d54179730b1d255fb82aa`  
		Last Modified: Mon, 29 Jul 2024 16:56:36 GMT  
		Size: 211.5 MB (211478612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:5a87517c14fa1f49801c9e77925e6dddf871f4edb2a1e812706f46f1a8cadb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2676532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b92d68875b92e48c53a1acf6ba57a89e6a7e5fd24b90523bdde981552c2644a`

```dockerfile
```

-	Layers:
	-	`sha256:b761dade46beae16be3db58296f2f3f134dd437c7f5c631a27d91ee2cf69662f`  
		Last Modified: Mon, 29 Jul 2024 16:56:33 GMT  
		Size: 2.7 MB (2659174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be192e29bd299787003078d1dffee2473f89deb23a21edca3d536e1d6f6cfc87`  
		Last Modified: Mon, 29 Jul 2024 16:56:33 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:41af259051be0cb1f75cd7de652d85449cf3dd3e30c64b6dd7b71b95876d6012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240982354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cc12d70f3858f7d19dd55281604b023dc23f067836cd051cffb29583522f5c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jul 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+34
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='9d3fa4fbb8247f3a47788c52c09ac5c265e023cfda821610ade2a43104bdaace'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='f79a40a5860e7b57ced61d19167847390dbe4f370c7511cf7923f75d4a546363'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3bd1e759a916e6497c78e1f9bc18301b82c1d8c089d5cd721ebc3c2f5e7f3f`  
		Last Modified: Mon, 29 Jul 2024 17:01:58 GMT  
		Size: 1.6 MB (1565920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2fbd257e1e0b42c67cde590380c3200afc7b7d1d0317770b94ce9ab1a703b6`  
		Last Modified: Mon, 29 Jul 2024 17:07:12 GMT  
		Size: 209.3 MB (209340351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:9917de24bcb3bd2f8a2c0b92c1bc40366553740c54362dc3241431cb35ef22fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db0309b2baafb3c86b06adde69c029f1da84a43e877baf844427e92848dc2f7`

```dockerfile
```

-	Layers:
	-	`sha256:9d867e79fbb1759315481ad95873be0abfba5222655a852cbae88302c999f58a`  
		Last Modified: Mon, 29 Jul 2024 17:07:07 GMT  
		Size: 2.7 MB (2659450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd98cea36f393c5cce539bae86761d86eddec51061149c9edb2428455d53b249`  
		Last Modified: Mon, 29 Jul 2024 17:07:07 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json
