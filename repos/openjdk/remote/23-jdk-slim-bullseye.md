## `openjdk:23-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:c7751410f8d3dcb3d586fedb430a54d83e54250c4fd19f3c0e1b475dfe8ec457
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:1096417b7d8d98b9df153d1541d6910611af60cf6b6172961ad55dd4a3eef9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244466961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c28cdcf6ae0f7f45a815a50535a689b5114e103cccc3f148b4ded7d463740c4`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 29 Jun 2024 00:48:10 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 29 Jun 2024 00:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_VERSION=23-ea+29
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='1ecb4977a7385dde5f7155e22cfdad0bec51afb8ff4dece08a061bab64be8aaa'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='a14bddc20e706cf85f28b8cc360e3dc2506b51cff9a0e62125f3213de6c41f00'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7f7ccff49c16870bdae9ef37cbad3893ac90d9b1b71e3baada96da4622c4c0`  
		Last Modified: Tue, 02 Jul 2024 03:21:46 GMT  
		Size: 1.6 MB (1581789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a5b99cfcfacda297370015ab897e0b881207fb1c5c6326a32e4bdd37d11bb8`  
		Last Modified: Tue, 02 Jul 2024 03:21:50 GMT  
		Size: 211.5 MB (211462888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:27bac8a7d063b6bce9cb61ba0ccb062512060ccb7d363aa6828edb1f75f7282f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ca73a695784c0d9b0f320ea9ea81d80e0b9ae3505fe3098e3d7871c15ab17c`

```dockerfile
```

-	Layers:
	-	`sha256:9b8eb8711d706f3f9efbac33bfc8ff1ad069bd69d82ca27334c228f1911e9d8a`  
		Last Modified: Tue, 02 Jul 2024 03:21:46 GMT  
		Size: 2.6 MB (2638497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b0523093f48ccfbe8444b60e98fbbc68664b9daa5b5e4a3acf0f0ea801daf8`  
		Last Modified: Tue, 02 Jul 2024 03:21:46 GMT  
		Size: 17.4 KB (17358 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2c221e66c78e7820a726e221613d5115f315b36291bde60b44d72fee70cb03bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240768982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034e828795089e93dc04df5e43559b6165d969e36314b849b58d65681f583bc2`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 21 Jun 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 21 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+28
# Fri, 21 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/28/GPL/openjdk-23-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='55c6ef3457ea9e056119ae7ab55e4691742458d74fbe1a1a7cdb7d08527bee1f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/28/GPL/openjdk-23-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='9844e3616fd6e16a94212badb2aee65f0a5805b43c587d80e9ae85174f18b984'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Jun 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8abb9c6653ca6c247cb904f25b084470905f4d6682db52ade7c408705b3728c`  
		Last Modified: Thu, 13 Jun 2024 19:58:27 GMT  
		Size: 1.4 MB (1361905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1e7f3633ec6468e4f6e95904ae82e186436efb104de9e6da8d20bb342cc59e`  
		Last Modified: Sat, 22 Jun 2024 06:26:41 GMT  
		Size: 209.3 MB (209320104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:02a7bab031e9eaf7b407fa0dbeced325e9209543fbadf8de2fcdb21bbdf01ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2656462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4191eba600d2fe914aa7beaae99b74882b7ff5dd473cb78e844b1da2fddb44`

```dockerfile
```

-	Layers:
	-	`sha256:03e69671280b20ff8aa7dd516113f1f33fa7024313c619cf3dfb9cdde36cdabc`  
		Last Modified: Sat, 22 Jun 2024 06:26:37 GMT  
		Size: 2.6 MB (2638771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71f83485410cf274b2b25a437f9bec7578c98eb23d6aa0be76f20555259b1a4d`  
		Last Modified: Sat, 22 Jun 2024 06:26:36 GMT  
		Size: 17.7 KB (17691 bytes)  
		MIME: application/vnd.in-toto+json
