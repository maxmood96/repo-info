## `openjdk:23-ea-12-slim-bullseye`

```console
$ docker pull openjdk@sha256:11e6323acf5b790f766278b5649aae0ce4e2a2d6aea3b4a943f04d43e1a4477a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-12-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:e8885e8b96de127b7218814f09dab1493038f717905d5eeeaa6e1be42e1f13a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236288788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5295f9a0dcdcf773921da53010c018b841e223bc2fd65f9c287b2c569fe2947c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 29 Feb 2024 19:48:15 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 19:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_VERSION=23-ea+12
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='892346bd29f50e248ab5980903e5759f73d8ac2b6ee0cd918e3acdb132eb8776'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e927b03ed3af88337e11918d05955c72b71c1664dc5791ba4a6590329004657'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f7e05a3997f07fa67fcf55eef19126a75d3cd688fb042f58593e8433ea022d`  
		Last Modified: Thu, 29 Feb 2024 22:50:30 GMT  
		Size: 1.6 MB (1581826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8918740011a92666f906dc095acc527b1a20a05e09c8b44b7b173fed1efb2693`  
		Last Modified: Thu, 29 Feb 2024 22:50:34 GMT  
		Size: 203.3 MB (203284537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-12-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:cd369eee38d4fdc688302aaabf9c761e2e91721188be850234ff7c02144116f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d60a0e273ff460d6ab6546c16ee53aef359e0190d5ef9ac451329f3f815568`

```dockerfile
```

-	Layers:
	-	`sha256:90c4ef1b4e3315e767dc760dc0d2af4f61c1d8689923b829223be03f275de9d8`  
		Last Modified: Thu, 29 Feb 2024 22:50:30 GMT  
		Size: 2.6 MB (2638332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4081e9b084249c780d78d43acad428be6da86b949b172a1c6fe6bacf33a190c0`  
		Last Modified: Thu, 29 Feb 2024 22:50:30 GMT  
		Size: 17.5 KB (17471 bytes)  
		MIME: application/vnd.in-toto+json
