## `openjdk:24-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:20a00d611febcaefdec836108770c6cba83bf188a84b1a86c0c510e6c2739197
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:d158ab3b0c47126c89b0c2be49f4bb9610b348531dd1db64bb9cac071000009f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244546315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738ceeb0396bc0b9675f878e4bb3e5637db67dbad8af5754df36766fc09a750a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Jan 2025 07:48:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 10 Jan 2025 07:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_VERSION=24-ea+31
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='fc69771e3af411ad5be33bf328a73b32318264a7aef1f28d1e6339cbf609819b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='5c35cd6370cdbe71bda96ccae35f3a74972b83dc6958e783b803f730b24f9a0a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012e23c4e4e031afb11927537f281ebc3a3ac736a4f2646be1d977cad8122f5d`  
		Last Modified: Tue, 14 Jan 2025 21:50:37 GMT  
		Size: 1.4 MB (1377215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc783e4ce1beebcaba2011a07d2411e2570ccbbb9b5a9f44b1dcff1eed16542a`  
		Last Modified: Tue, 14 Jan 2025 21:50:58 GMT  
		Size: 212.9 MB (212916435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:9995f278248d985327f75ffa215cb849d8fdff5a83670a6f47dbe77f6ff80a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bae284bb059a9c572ad52921a7fad8b75f276c0e8e8f201e78eb3a7a6ea4cde`

```dockerfile
```

-	Layers:
	-	`sha256:2f15b348851fe79e346a117e77ca2010303865c2530298318c76af0d60c55db7`  
		Last Modified: Tue, 14 Jan 2025 02:36:44 GMT  
		Size: 2.8 MB (2827922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ee7d07fd5d8d92ab05a1008b1d69a150b7fa8a2fb8eb9f0d30d67f7899864d0`  
		Last Modified: Tue, 14 Jan 2025 02:36:44 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a4f46000b67db476f70ba00caec54f2c657455d273a44037c78ece1923ddcb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240979043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc70d131109fda6ee6d32845554631c23b287b31409424d35576b77e7c49b24`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Jan 2025 07:48:13 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 10 Jan 2025 07:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_VERSION=24-ea+31
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='fc69771e3af411ad5be33bf328a73b32318264a7aef1f28d1e6339cbf609819b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='5c35cd6370cdbe71bda96ccae35f3a74972b83dc6958e783b803f730b24f9a0a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1401c2185a5f6b10d74a84de713de9f232aa9ed5f90f55098b0de741737421d6`  
		Last Modified: Tue, 14 Jan 2025 07:44:51 GMT  
		Size: 1.4 MB (1361281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a967f9da8d788ce5f2fb22d044ade832910dd2ab5c54209bb7ce1249faade407`  
		Last Modified: Tue, 14 Jan 2025 07:46:45 GMT  
		Size: 210.9 MB (210872849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:2bbebb90a9bddaab2125974914e7f8e1a8cd3fcbe85651c8ab7714faaba26848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de343f1d069b7ed3b35da25f24547c7bca4e1b7f3d28d9b36ffb1654cc2218af`

```dockerfile
```

-	Layers:
	-	`sha256:b190ac351d5d03b8011df520072d4768bf482b27fcb86aca075b03b0af5dfe0f`  
		Last Modified: Tue, 14 Jan 2025 07:46:39 GMT  
		Size: 2.8 MB (2827574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c84d7c0a1403cfab7720743e3f77c1a2337f5b9daaca9f71a26d5f28ec47a9a`  
		Last Modified: Tue, 14 Jan 2025 07:46:39 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
