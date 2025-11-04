## `openjdk:26-ea-22-jdk-bookworm`

```console
$ docker pull openjdk@sha256:f17e85ad04c4d184f086f51c725b07eba4666787ee2cf39d873130e407d50d77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-22-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:92057521db55488fd1553804a3967fcbb00a02732d94098a21186cc21c34dd10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.8 MB (379765098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d090c2c4ca898c4f2c87cd3be743f0b974f982306ad43446f77cac099d2272e7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:54:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 07:54:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 04 Nov 2025 07:54:29 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 07:54:29 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 07:54:29 GMT
ENV JAVA_VERSION=26-ea+22
# Tue, 04 Nov 2025 07:54:29 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Nov 2025 07:54:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2123190679e81d983648da92f1bb9ddc74383512edb00ad64f93d24d00d8807a`  
		Last Modified: Tue, 04 Nov 2025 04:14:49 GMT  
		Size: 64.4 MB (64396145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22abd8318b7c1db908d8c88bd64c75c6c7cbc3756a3c5e072bb3c0abf268c8a7`  
		Last Modified: Tue, 04 Nov 2025 07:55:02 GMT  
		Size: 16.9 MB (16943580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ce091065d73d9c35a4fc27a4460babedb59ffaf90e815b1d1ffffb634304a6`  
		Last Modified: Tue, 04 Nov 2025 10:24:01 GMT  
		Size: 225.9 MB (225915016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-22-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:aa41d7289bff5289f91134fee4f2edb04fd1bb38fedf0715598161b8b828d062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f198f94b971d848e839cc5ec361d16524db1314c992fd836c363b8f54247d6`

```dockerfile
```

-	Layers:
	-	`sha256:b6dfa8319378c7519f92fc30a35ed41846514964fd029a448e3d2554e0b29ab8`  
		Last Modified: Tue, 04 Nov 2025 10:23:21 GMT  
		Size: 8.7 MB (8668833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e635c1e2579828e2e3a86b5f2135e153ee079ac40e97685578fe4fdb1cbc06a`  
		Last Modified: Tue, 04 Nov 2025 10:23:22 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-22-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4d1e550a2432e541238c5cd047a2392c3aa77eec5c6a44f7cb813adb4b66cdf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377825172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc73371ff28713acebc5997b00e0610d8f568ce780099ee59a3c35f6cac445e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:33:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 04 Nov 2025 02:33:57 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:33:57 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 02:33:57 GMT
ENV JAVA_VERSION=26-ea+22
# Tue, 04 Nov 2025 02:33:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='b87eeeb2167b024e3e62fb5ab860c0e2ad004d2e04f716b9f885d1180ac97a03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/22/GPL/openjdk-26-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b401cd0d932a4b8fd19f44deb517bfe9441097f31a2bbdb247e3b8757772e147'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Nov 2025 02:33:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020f0f7f102dcd1ca7603a86d7398adbe5369a820cc6f32954c0b3b5e2ac7403`  
		Last Modified: Tue, 04 Nov 2025 01:30:05 GMT  
		Size: 64.4 MB (64371335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef3edc076795524a415d52bc44d331551ab2b5db38b9004ed87b60a6415b8c7`  
		Last Modified: Tue, 04 Nov 2025 02:34:37 GMT  
		Size: 17.7 MB (17727668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7855319c69afeca342b4bc978ecc4bfed3d0dea3cab5c8306271225cd417fb6a`  
		Last Modified: Tue, 04 Nov 2025 13:35:42 GMT  
		Size: 223.8 MB (223768177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-22-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:8bd35afcf9452f46054bcd8e94ddfe024887dfc1cb1b054f62a8148b9f21e5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35ac85e34f558bfc9c4f4e7df73f354cf5780cee1bfea948ec9596cc7813530`

```dockerfile
```

-	Layers:
	-	`sha256:6cef0bbc4b3ff427f3059541b7a41967e0cddfcb0a960812fddfbe849a320e90`  
		Last Modified: Tue, 04 Nov 2025 10:23:30 GMT  
		Size: 8.8 MB (8805678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f144455b0b353d1c010c546eeb47c96ee6c9b844b3fff9da11c72229a1118e8`  
		Last Modified: Tue, 04 Nov 2025 10:23:31 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
