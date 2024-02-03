## `openjdk:23-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:f3d67b1421f2bc3f3932ee75341687c8d63035eb7a29916ce4ed518a70e34f48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:b542cb18a9c1763089229a678fd95ab3dba672c61d28769864443aba933210ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236099216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6ca1fca7eeb757282be22d72d77f67826db2ad64f161e84a7041f55c93f0b2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 02 Feb 2024 19:54:38 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:54:38 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='3f36f003a7dbc52c00e66678dfd2c190be7939f729e85db1848911f3f3e61704'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='a216441b0aeba416ff109cf7eb4337ce00c7f4eba5e77b0b45a1b79cde736690'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f40d836cdc5e18b29d31457512ce76dc10119d7cf14bd0320ec32629c61aa58`  
		Last Modified: Fri, 02 Feb 2024 22:53:38 GMT  
		Size: 1.4 MB (1378085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be337dd925b818ff3e52cf0b1200accd08734bd9b6ec7e53f74bea32c5516a5d`  
		Last Modified: Fri, 02 Feb 2024 22:53:43 GMT  
		Size: 203.3 MB (203303304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:001f343b6652fc3c772cad1d8c77038c5bf7ce90388ed1e3370200e80e40ced3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4663268b63ac5293e1d2046b6c6bb2db1a17db258fe0cd5e01e4338240eb494`

```dockerfile
```

-	Layers:
	-	`sha256:d7061a11c81e029c37eeb865116e7d4f9eb656dd06f05a6d9aeac0e012833a6d`  
		Last Modified: Fri, 02 Feb 2024 22:53:38 GMT  
		Size: 2.2 MB (2190188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7558a81f79211d028cbef7b185ee3fc73f08f8e87b380ea3c339cb460f7feaf3`  
		Last Modified: Fri, 02 Feb 2024 22:53:38 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2146fa709e9798c253e82a548a0a1915a1eec0c8b9a91110618eaf518d14fc1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232610308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfda1c11422230b0f2dd854d28296736ca3408f70d2696c36e1ffaabd25fc34a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Jan 2024 01:56:28 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["bash"]
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jan 2024 01:56:28 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:56:28 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='b10ac9dc80cf8dd508c44072989f1327a05a95dfcbf0af1fc65571ac2de613a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='b21ca578927851a80700167439bbb9cd75c7d60152d51240bac49be8dd548e7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3bc7f554a0ea1458559926cfeb111c558c33065ef21aaaadc2eb1182f2acd0`  
		Last Modified: Thu, 01 Feb 2024 16:21:04 GMT  
		Size: 1.4 MB (1361927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becb9036c8c87c79c9384875e8955fd41e2533845f085ac8f64243f0233cff8d`  
		Last Modified: Thu, 01 Feb 2024 16:21:09 GMT  
		Size: 201.2 MB (201184047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:1ee0923e37aed656fee871b501102a8e46c56abd35947470ae73366628e86fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e755d47f8bf68fa95c5f4049f54b6444be81830b4898b833fab1a70c08195b99`

```dockerfile
```

-	Layers:
	-	`sha256:0c98a40d2d0cf414c4b802c6e57b1c4573385c77cdfa3dc6cfcfa98525c9e628`  
		Last Modified: Thu, 01 Feb 2024 16:21:04 GMT  
		Size: 2.2 MB (2189543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:029ae3d71b86316c618d243a0d1f4f258621b76d64486a64c6b028951fc812b7`  
		Last Modified: Thu, 01 Feb 2024 16:21:04 GMT  
		Size: 17.3 KB (17305 bytes)  
		MIME: application/vnd.in-toto+json
