## `openjdk:23-ea-13-slim-bullseye`

```console
$ docker pull openjdk@sha256:aa6c12c82a1afe266022aeea09bf5dbe050bf609ca9acd129e9c7821ba1a09f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-13-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:b412bbb8dd4fb6a05ed3028272ee69878f12ae9dedd300b088bbde2002d915a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235977332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94f752ecaf45903546090f3b6adbca68a4f560c8485e0691bb3dcde723f6db0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 01:48:16 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["bash"]
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 08 Mar 2024 01:48:16 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Mar 2024 01:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_VERSION=23-ea+13
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='f805f5ac203384c50ac3980796a4c4d92d1e21b0ead0c9870e1ed8edc9e2588b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='061adb6d88422017ef07f10561bd9b551f22e36b7db0860e1505900d8f5165f0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132b5334d0ecf3b18760322de8be87c75fadcb603a133fdd26e39a5b5ca23019`  
		Last Modified: Tue, 12 Mar 2024 01:57:06 GMT  
		Size: 1.6 MB (1581835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5574d7c8c1ced772436549d88ba4b6de21e8869013832c4093943958d0fe2c9f`  
		Last Modified: Tue, 12 Mar 2024 01:57:08 GMT  
		Size: 203.0 MB (202973008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-13-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:982d353e147fe389a04449e280e3bd91edc359fa34b723316a16270e47a18a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30a754537f26b8972836a5da6104d21e17044a8dd4d7df77b3772180df48ef6`

```dockerfile
```

-	Layers:
	-	`sha256:88a83916e76312f51632d42fedea3ebd0779c125bdd980e461936565075eb1fd`  
		Last Modified: Tue, 12 Mar 2024 01:57:06 GMT  
		Size: 2.6 MB (2638332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1639f220bc4fbe30a566acc92359fb1f8f1a729c73e40fcb11442b1b5f41695c`  
		Last Modified: Tue, 12 Mar 2024 01:57:06 GMT  
		Size: 17.5 KB (17472 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-13-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:84e34131742b00b7e34f510029eaa30e8d7e472decc7441e6f5fb1fd1aaf2e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232479341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58a66ad7ffa317ad138e3cf17d6f89e0e17efad012a442739f4e94a5cbf6935`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 08 Mar 2024 01:48:16 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Mar 2024 01:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_VERSION=23-ea+13
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='f805f5ac203384c50ac3980796a4c4d92d1e21b0ead0c9870e1ed8edc9e2588b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='061adb6d88422017ef07f10561bd9b551f22e36b7db0860e1505900d8f5165f0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db00f1057908790545d650d77cf39618ea1e03919fed252c37292943bafda3e`  
		Last Modified: Sat, 09 Mar 2024 04:01:31 GMT  
		Size: 1.6 MB (1565928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2886f2bdd28ea6783132200c40b6d980fbb6b8a5eea7d78b102bfe5c4ec79c6`  
		Last Modified: Sat, 09 Mar 2024 04:01:36 GMT  
		Size: 200.8 MB (200842336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-13-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:507d7aeaa23a35a59c212147bf91a78f619b3a90441cacc32a8d5989d72656db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2654905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e3186b814cf406133aea7828f1c17ed61f94c6ae37051f39b7444cf690414b`

```dockerfile
```

-	Layers:
	-	`sha256:d99103c356fbd9c96f9d8fdcd0c98d641745e1cf6bd8bf15cb23f8bcfee255ca`  
		Last Modified: Sat, 09 Mar 2024 04:01:31 GMT  
		Size: 2.6 MB (2637586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebdceb4a39c5d0ba3ca8492cecb114ecbe39e42c15a382c1517f6e6f212717f0`  
		Last Modified: Sat, 09 Mar 2024 04:01:31 GMT  
		Size: 17.3 KB (17319 bytes)  
		MIME: application/vnd.in-toto+json
