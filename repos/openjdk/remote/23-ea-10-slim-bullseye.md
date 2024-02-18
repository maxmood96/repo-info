## `openjdk:23-ea-10-slim-bullseye`

```console
$ docker pull openjdk@sha256:2a87c355b73bf6b07412bdd1afb87a895246183066a90a2473ef9fd801ef9ce5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-10-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:5babb2cd1bbb8cf646bf38bc19a4cbf70b69ab9a61bd69d8ce517a384c08190e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236270838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e65379e3f4d99fce84017eeac9726ae6fb44d6e9c85b0b822ee465e76268225`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 16 Feb 2024 20:22:31 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 20:22:31 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_VERSION=23-ea+10
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='9b583a20351ff9be1b782ba71d5e61d7f8e4731c81277e4f2566c5509db052b0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='b646bcb58d932236e066c97dbc32d6df53a9a823c78565cd22bd6bf05a0cea7d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42976b62729917f690718b37decc28e3cd9443667fe3c7a44512c59efad6719`  
		Last Modified: Sat, 17 Feb 2024 00:53:26 GMT  
		Size: 1.6 MB (1581815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a1432622ae6ceb6616d116ae7150fd56ed2726710d45c206e87431e22f2d60`  
		Last Modified: Sat, 17 Feb 2024 00:53:28 GMT  
		Size: 203.3 MB (203266598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-10-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:5f3fc0626538c5208b9ddafddf9f6e456aaa9d4e648bc3ad7994a9606a70ef53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b4c4d0cd775c4c424a13dcfaac07a1e41223e803d71aeea14957e26b1c661b`

```dockerfile
```

-	Layers:
	-	`sha256:62a59d2c9edfdf4b127396fcf12f65c984eb8e764c959973f795474fa64101e9`  
		Last Modified: Sat, 17 Feb 2024 00:53:26 GMT  
		Size: 2.6 MB (2638332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555269c3f7e1471518fb79ac5ebad74bf77911aefc6741833119a36f47747f3d`  
		Last Modified: Sat, 17 Feb 2024 00:53:26 GMT  
		Size: 17.5 KB (17472 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-10-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4060897609e215f8394627c63e451e46c4f19165800e4e9383465426b089f499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232782298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024cc87e255d9d0bc3b2e86360064026919a3b921524aee6587c10d0a12fe2c2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 16 Feb 2024 20:22:31 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 20:22:31 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_VERSION=23-ea+10
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='9b583a20351ff9be1b782ba71d5e61d7f8e4731c81277e4f2566c5509db052b0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='b646bcb58d932236e066c97dbc32d6df53a9a823c78565cd22bd6bf05a0cea7d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66665e7107836c004c0e092f793e4525c11b530024a61f362798cc6f7500ab93`  
		Last Modified: Wed, 14 Feb 2024 01:18:12 GMT  
		Size: 1.6 MB (1565944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcb0320449ed687b8b4739750f898d03c43069fe58ab2b0351e9eeaff6b19a8`  
		Last Modified: Sun, 18 Feb 2024 05:20:14 GMT  
		Size: 201.1 MB (201145277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-10-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:f251db9122db3f734a49625fff438c0ee1b5df76eecbfb8e4a17a2a9f3f2f056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2654904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f83d70d7684dc585731d57487194e6dd45e4cc2c17326404abb246e29ba87f`

```dockerfile
```

-	Layers:
	-	`sha256:8873a874b44370b086384bdac5f7b912e3525c6c1105a7cc626c5a5ebe5faa26`  
		Last Modified: Sun, 18 Feb 2024 05:20:08 GMT  
		Size: 2.6 MB (2637586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adb3208380ca53f4e95062dd7ada3a66a964dc22b2e2a30589825f0908e73b26`  
		Last Modified: Sun, 18 Feb 2024 05:20:07 GMT  
		Size: 17.3 KB (17318 bytes)  
		MIME: application/vnd.in-toto+json
