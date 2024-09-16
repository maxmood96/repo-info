## `openjdk:24-ea-15-bookworm`

```console
$ docker pull openjdk@sha256:8a1db29c02a77efff799f71be3da56b186cbcf32d8dd318deba95e95553ba432
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-15-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1564844bb4bba8117186d6e1772f5c84ff784be0eefc86612c14f0d7879f3bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364723027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a9b916d8e0c4b5fc89f72fc492382e9f5aede96ec35719e94ddfaaf61123b7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:01:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 14 Sep 2024 06:48:15 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Sep 2024 06:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_VERSION=24-ea+15
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='b41d4867c348d7f1991085d8bcc8797eaf032d9dfaa3419bc9db15eaea75e91e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='165b7c19403e9708ca261cdfe4c385e837df683049203e33ad2bf76228054a25'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843b1d8321825bc8302752ae003026f13bd15c6eef2efe032f3ca1520c5bbc07`  
		Last Modified: Wed, 04 Sep 2024 22:08:14 GMT  
		Size: 64.0 MB (63997467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b6f012ccff6ca072ee648eeb669eb5d011cf0f400da82a947223b15780d28e`  
		Last Modified: Mon, 16 Sep 2024 19:22:31 GMT  
		Size: 17.7 MB (17727278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3935803c5e56398446ce8ebf3d7e202186588f6e8807a1319afc7fa777025179`  
		Last Modified: Mon, 16 Sep 2024 19:22:35 GMT  
		Size: 209.8 MB (209818380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-15-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:21d64c8b6dbcaf89cf3a497c0c3cabf4ab10425da5c78941ff354a0f49158455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8413842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b3e5abe9b4d00434cffc0d97d6cef0f1153ebc1444a481fd6ef54a46f84bc2`

```dockerfile
```

-	Layers:
	-	`sha256:9180736ef75db45e4e3a5f013ba5746ffea24009af37b76b4bcf5b28235f7583`  
		Last Modified: Mon, 16 Sep 2024 19:22:30 GMT  
		Size: 8.4 MB (8395040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1edec73c68a1ca2c5301cc499ce43b5e7af0c7551de3d9abebaf8e3f50c11ed`  
		Last Modified: Mon, 16 Sep 2024 19:22:29 GMT  
		Size: 18.8 KB (18802 bytes)  
		MIME: application/vnd.in-toto+json
