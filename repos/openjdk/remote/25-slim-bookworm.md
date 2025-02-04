## `openjdk:25-slim-bookworm`

```console
$ docker pull openjdk@sha256:60090627d21a8c1d297d975452aba693e17d8f98d4e67a4724ded55aeeaa739b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:c07be4a76758307e8d5a9323e11b01e4008a3b1a89d83a1cce47ecc65498c923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244165683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413481b2d4de13b23dac435d813f4e664417df0f55789f1629d403f8749b37be`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Jan 2025 01:53:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 31 Jan 2025 01:53:00 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:53:00 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='1463f6f26464b27899d02c4bba0e2eb7f8b8dda88afb590c31c882a4ee3aeb68'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='fa9c00fcd40d033dce2058b91f5c8b689fc492bd1f0c6062729915d333b82ff1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b1e970d9b2de95b50b2a9ecc79b2ed452ff9145266e6ea0c98d435c71830d1`  
		Last Modified: Tue, 04 Feb 2025 04:43:36 GMT  
		Size: 4.0 MB (4018418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2094e13cf988b8ee71c97abcc9207dcd6862a0af95e10fe97120b7f48f8248`  
		Last Modified: Tue, 04 Feb 2025 04:43:40 GMT  
		Size: 211.9 MB (211934962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:5fdd8cbdc8c91f49e961ec2d47710d0b7e3cc2b85d4a2bacfd8d52ee98ce182a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff4f10b7f2b45563be9686f0872620a56acbeb29898a2dba8347c2c1c4b0876`

```dockerfile
```

-	Layers:
	-	`sha256:dc025a3786d35a9c57868d4918cd2b751dbd4722cbd6e0155ff0ed05ff8c41b3`  
		Last Modified: Tue, 04 Feb 2025 04:43:37 GMT  
		Size: 2.5 MB (2533878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4db58887d814db4c20dd095cf81507ef432080dc7c845de26e7228cdded04822`  
		Last Modified: Tue, 04 Feb 2025 04:43:36 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1b0e65428ef7f58f9830d87a4fad2320291327c3ab17bbeb8b1de4f2cfb1f2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241780199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954095511433030798ba85393f2182a027cbeb529a30fc52263670a642449935`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 31 Jan 2025 01:53:00 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:53:00 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='1463f6f26464b27899d02c4bba0e2eb7f8b8dda88afb590c31c882a4ee3aeb68'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='fa9c00fcd40d033dce2058b91f5c8b689fc492bd1f0c6062729915d333b82ff1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f083f07e13bd63cd44a785caf631d4e023799e01a18898c1a673879d76b06aa`  
		Last Modified: Wed, 22 Jan 2025 02:34:57 GMT  
		Size: 3.8 MB (3833715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d56781723878c4a8525922c4f2db1ca6b7b9f99eff8a33a34bf639056f6ea5`  
		Last Modified: Fri, 31 Jan 2025 22:29:06 GMT  
		Size: 209.9 MB (209905453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:10901d756166a29b26be71121efb741d87d00a1f74db32a43027f8585c735ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b18c859510c9a38e0e0ec8ebdc6ce033ab908025c2867c542218650e585965`

```dockerfile
```

-	Layers:
	-	`sha256:89d190829a951ecd0d8019604306c238afd8cddc8b93f0fde9087bdd568a324f`  
		Last Modified: Fri, 31 Jan 2025 22:29:01 GMT  
		Size: 2.5 MB (2533608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3bc2054ecaefac64ba85a89f048ddcc5649859712debe1ab8f3e05b742763da`  
		Last Modified: Fri, 31 Jan 2025 22:29:01 GMT  
		Size: 19.6 KB (19640 bytes)  
		MIME: application/vnd.in-toto+json
