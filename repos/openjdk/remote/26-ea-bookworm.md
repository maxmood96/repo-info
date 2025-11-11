## `openjdk:26-ea-bookworm`

```console
$ docker pull openjdk@sha256:6ef984715c5aa89e5fc5ea95b5caf741b9bc0cbe6dbe95b6f7ed800e24f96460
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:4b5f971c7cdd4917efffa0c4eda8f96fbbd775f19cd1582eaba78b121d520f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.8 MB (379799365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537958bff08305a849d0de9b03961686912b2d7192d006fab10634fde57e049e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:52:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:52:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 10 Nov 2025 19:52:44 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:52:44 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 19:52:44 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:52:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='c5cb587a920ddf65225352cf2494965786acd1de8d6748a976d7498d0783a396'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='427f53a6635347b853f695324253b6d78f69cc09334a9cb1031a801e43358883'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 10 Nov 2025 19:52:44 GMT
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
	-	`sha256:0fbc2dfa5b52c6a2d69a14c37877d41c36482d67cbcd3b8e85c69a40f75047a8`  
		Last Modified: Mon, 10 Nov 2025 19:53:25 GMT  
		Size: 16.9 MB (16943651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f370f3729242d4da3abd4f15b5f7a62731663994056b9f0560181085fdd7fa8`  
		Last Modified: Mon, 10 Nov 2025 22:31:27 GMT  
		Size: 225.9 MB (225949212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:cd9628aca4ad0494a1978bce9d069ccf0a8ba9a6dce59fbab3723060426f149f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8200273921fe8604c33699f5f6db249f91d129c2435220322522f179cf97c70c`

```dockerfile
```

-	Layers:
	-	`sha256:a45f79e4a55bc6787ba772e5c954e8af188cbaf4dd54375a11ef53a348cd74ef`  
		Last Modified: Mon, 10 Nov 2025 22:23:37 GMT  
		Size: 8.7 MB (8668200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf98beea917dd9e9509409b4837aff3a9e29709e5c072b61d5f4030c47b8f146`  
		Last Modified: Mon, 10 Nov 2025 22:23:38 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f6877030da4a57c294af49c160a5b1db366048bd024deac77f0ac90ed0e09687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.9 MB (377860445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1498eb48b98eeeedf5ed164f13c0ff4b912327b4abc83170b512adaff9fdf6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:53:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 10 Nov 2025 19:53:01 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:53:01 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 19:53:01 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:53:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='c5cb587a920ddf65225352cf2494965786acd1de8d6748a976d7498d0783a396'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='427f53a6635347b853f695324253b6d78f69cc09334a9cb1031a801e43358883'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 10 Nov 2025 19:53:01 GMT
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
	-	`sha256:f4ce1a5497477dbe1316ff85f41c920ae9f0cadccca670b062cdae0c471401ae`  
		Last Modified: Mon, 10 Nov 2025 19:53:39 GMT  
		Size: 17.7 MB (17727705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7870f3051f470e29b568b7decf5e6f0b5a0815dff85a557b1f871d47cd4393`  
		Last Modified: Mon, 10 Nov 2025 23:08:14 GMT  
		Size: 223.8 MB (223803413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:66c41f013afd9fb19fcbd84fc0c863a2a33e1a9424c40f9db65baa2d8010961f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243a96454e599d51c41da0d1af577cb737b9dbf1632b55dea0361cb08b7585cc`

```dockerfile
```

-	Layers:
	-	`sha256:d6657737b8b07cdb21dc5710490574cf5a43d4b5421d8d10df82bbf64618862e`  
		Last Modified: Mon, 10 Nov 2025 22:23:45 GMT  
		Size: 8.8 MB (8805045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a2c9e676a1f59f53d33f723ff3eba346b749318c09afd3a880bcbf35815d144`  
		Last Modified: Mon, 10 Nov 2025 22:23:46 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
