## `openjdk:26-ea-slim-trixie`

```console
$ docker pull openjdk@sha256:63814a9d8bbea6d39d5ce9c91843bec5e9d9d1d1bc2bade4bb57ba70c0839553
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:29d696b3014428c1ff956319f7b272e574178c314871c565649dae0ca40f1040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258052344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:330db8d6dbe8b4a4b2112d483691abfda39c0fb9306ead3d542acc0e8ee5606c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 24 Oct 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Oct 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_VERSION=26-ea+21
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='3189ce7f96b6fb0b69ce1e8ca7bc626aa30009023f9e2ddf7faeaa5ddf9e8626'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f2d4dc408e6fe82574fb9ad9cff97da63a897a887198c666cb1bd0987fa690c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5af5e27ba1f1a0ec83f9de047bdb8c2c57dd64edb8bf83a6d7522da38c067b`  
		Last Modified: Fri, 24 Oct 2025 23:22:21 GMT  
		Size: 2.4 MB (2371146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04ca1ad778f2c7ada1b66b807d048ed6fac3f37f879bd14f1a379c8167dd0cc`  
		Last Modified: Sat, 25 Oct 2025 00:31:21 GMT  
		Size: 225.9 MB (225903274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:8ca75bcac9aeae87cbc35ae65e0d05911d75a321fe4b43830db5b74264111720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e27ddc4d99da99b9dae0fe701f3728c1f310652b0491e322fceca394c8888a`

```dockerfile
```

-	Layers:
	-	`sha256:3861216e28dd97a7a1331d7fdb003f57fd0e4ccd9b71eadd31f22f391e86994e`  
		Last Modified: Sat, 25 Oct 2025 00:24:06 GMT  
		Size: 2.3 MB (2281309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff70f3951b42ebd0dd7041b1409d2be090440a9558da8a22c73afd423afb0334`  
		Last Modified: Sat, 25 Oct 2025 00:24:07 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2c161f47784596d7b1e7f6407bcd4e630631c689548e9317b97498714bf6ab82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256203262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43257df3a13cc4bdef4f6471d0b83d8f29a6df528c802e3e3f4d7e8c8a267598`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 24 Oct 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Oct 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 24 Oct 2025 18:48:13 GMT
ENV JAVA_VERSION=26-ea+21
# Fri, 24 Oct 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='3189ce7f96b6fb0b69ce1e8ca7bc626aa30009023f9e2ddf7faeaa5ddf9e8626'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f2d4dc408e6fe82574fb9ad9cff97da63a897a887198c666cb1bd0987fa690c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 24 Oct 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a30ee89ac70a0000436226d94861c8e7f7c18776d85e19827f00b04d5536226`  
		Last Modified: Fri, 24 Oct 2025 23:24:50 GMT  
		Size: 2.3 MB (2314306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa84fa3e47b86a961362770f9b43eccad44ce77c52daa92b646cdb20aad208f1`  
		Last Modified: Sat, 25 Oct 2025 00:41:22 GMT  
		Size: 223.7 MB (223746829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:f5291396bd9b9242b79938502db36c387a0567a7fc82675d7ba5f8351be411ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1625f3d15280d9ce54ddcf007977f9f185fd8997ccab0059d6146f590f532473`

```dockerfile
```

-	Layers:
	-	`sha256:059040d5149edbff5b579f9a6a23fc96d96eef6cf51b5b84bd53743ed3ea10b2`  
		Last Modified: Sat, 25 Oct 2025 00:24:11 GMT  
		Size: 2.3 MB (2281043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf4f3ed28dc340ebe4b17ab98db4ed6161dda076915f9a2ce0dc2dd22774978c`  
		Last Modified: Sat, 25 Oct 2025 00:24:12 GMT  
		Size: 19.6 KB (19624 bytes)  
		MIME: application/vnd.in-toto+json
