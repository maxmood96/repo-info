## `openjdk:26-slim-bookworm`

```console
$ docker pull openjdk@sha256:564fa6e5852483dcb64cf11cc756c790845a8da1ecab86c1f26eb68299ec11fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:bf4fe04b4c7c0ef8e12725475e9e96f7a4ba01fa140c69093984c68df56357f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258119743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797349038c6817a8d6d4bcd7cb0b3e261109c2d0d46f320462fd4c7061a3cb3a`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 11 Oct 2025 00:48:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d943a6c917693cd9b5ba74d6837c2eea1fdb788aba045b145e19024c192d4ed6`  
		Last Modified: Tue, 21 Oct 2025 01:49:40 GMT  
		Size: 4.0 MB (4027311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77e12b6692eee78c8cbf1c635850e56a80a4c89e7a2f602d08af3d85728c720`  
		Last Modified: Tue, 21 Oct 2025 03:25:28 GMT  
		Size: 225.9 MB (225864111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3e867fad3f582b913345849bd7826933e3df2b3075b1b3d14044eaf1a08a2723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2670518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15420f1447cc60bdb4de7afb5b7f338a7bd2ee05dfaaac8bb68bac8321d277b3`

```dockerfile
```

-	Layers:
	-	`sha256:6ea79ec7d67f6a8b014a31303f57015c94f1175c9416b372f20e698977bc99ff`  
		Last Modified: Tue, 21 Oct 2025 09:23:44 GMT  
		Size: 2.7 MB (2652948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f2b7c8deb58279d994262e5486ca24dc8fce2b61c17cb0f952fa38af2bbe9b3`  
		Last Modified: Tue, 21 Oct 2025 09:23:45 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d18bdb81d12efc7bcd5c7ee1cc901deba8150b95aa0d107017608065ceb73b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255676716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b723f1e1fe94699deb4cb54511fb2481f0d115040206f10a5b58e5321a6cd5`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 11 Oct 2025 00:48:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 11 Oct 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 11 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+19
# Sat, 11 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='9a89dcca644d59f40b82f6712c854e416d5b5fe80808c40868e1ba2d6d8e1e9e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='2841b9fa0e22671fc0ee3e6ba1e87237d895446e7548021004f201a1ff5abd99'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 11 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa42d2dc4dc9ba2549a60ea962d367c617a9d8ce67bf267f31fdd8b1c82d81be`  
		Last Modified: Tue, 21 Oct 2025 01:54:17 GMT  
		Size: 3.9 MB (3851371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afcdd8bdf015f673c06e3a725df70da4399bd71e816cb1770241467e86b8662`  
		Last Modified: Tue, 21 Oct 2025 20:00:36 GMT  
		Size: 223.7 MB (223723155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e9b888f546f5836f7c523a1d4dc99295035db370e010062a4c5fe691112e4f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2670319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2970bb772f3a24db64f4fcbda7b4b5d1ac10196e2435be801d200a2a6e3729ca`

```dockerfile
```

-	Layers:
	-	`sha256:29593d0b111f8560b22a7af23f5d116e159dd1d8a04138b3f6cb0b2460732448`  
		Last Modified: Tue, 21 Oct 2025 09:23:48 GMT  
		Size: 2.7 MB (2652606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eb70c9f4d57cffa59bdf31d0198f8ac7d425db66be3054def8a68bc1a06aa21`  
		Last Modified: Tue, 21 Oct 2025 09:23:49 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
