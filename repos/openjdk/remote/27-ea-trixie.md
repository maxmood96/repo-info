## `openjdk:27-ea-trixie`

```console
$ docker pull openjdk@sha256:650f70bb3bee7bff1e76efa71dc705fd4d510518d6d8f80ecec4c4006e4d5709
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:fef5378c701b0197aac352b6fc21bc86998de41fbdd34fe989e750f4f19ce479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.7 MB (387710675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678217530562cda275dc1c32fdf6dc43c2c8101144d36f19d5088c5db347dcf4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 26 May 2026 19:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:09:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 26 May 2026 19:09:11 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:09:11 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:09:11 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:09:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b7ef4c5d5b31b1da3d1ffaa1101173333c25937f5db7d8b150e7b8a20bd70cb7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='fc322d442a40de5c1b80f1d8340212c8945e424693fca39a8006accd3427bf59'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 26 May 2026 19:09:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a988d9bf49e8b59c4679ba8139a37a6a5921f59f754d38d63ee53b6837b27c6`  
		Last Modified: Tue, 26 May 2026 19:09:34 GMT  
		Size: 16.1 MB (16065736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614a4a6fc264addcb56edd6d5b933a9c1e6d7584fc1157dc843313ec01b314b2`  
		Last Modified: Tue, 26 May 2026 19:09:40 GMT  
		Size: 228.9 MB (228922669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:2b92e98ba12f7cf6223cf2b1c96bf5ab999192d36086c8caf663e0142fa7495a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77150988fc798db5df795317f5edfc18b04fb7f936ff8e5c49b264164830147`

```dockerfile
```

-	Layers:
	-	`sha256:f763c06b6c5326d5ed253f3ee6d0d02c8e121f15b1463493ccea3e57145d13ff`  
		Last Modified: Tue, 26 May 2026 19:09:34 GMT  
		Size: 8.5 MB (8510074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d05059c5330a8ba6fcc47bfdc05da47f9603c1322af7ecdcd72bb9759b43d53`  
		Last Modified: Tue, 26 May 2026 19:09:33 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dae7cabf7159807476b2b18da1cafc6bb74d08876a0a319a7492dfd5a2ea7d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.2 MB (385248182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f13739a42eff6c3e467ac20b2cec53366b33789b5be170d865592605a6f4cf3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 26 May 2026 19:11:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:11:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 26 May 2026 19:11:24 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:11:24 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:11:24 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:11:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b7ef4c5d5b31b1da3d1ffaa1101173333c25937f5db7d8b150e7b8a20bd70cb7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='fc322d442a40de5c1b80f1d8340212c8945e424693fca39a8006accd3427bf59'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 26 May 2026 19:11:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4aacc853467140b486934cd504d3d865bee03b235fce27718bf3d99a7d6b0a`  
		Last Modified: Tue, 26 May 2026 19:11:50 GMT  
		Size: 16.1 MB (16071377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09683588aa4fae02524342b6c55a8b6878690f1fbb73d7ef7bd8901deccbdf`  
		Last Modified: Tue, 26 May 2026 19:11:55 GMT  
		Size: 226.9 MB (226886130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:dee5683a7b00d4c19489341d9d4230633e43459306218454e18b352e9b1863fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c0b0e5488b55d9e632e8706b29ba5d8cd759a3757081ab4aaa183c02c302ba`

```dockerfile
```

-	Layers:
	-	`sha256:534a7052c0032737620b963c6b98b190e29f0a6e3d91c9d13fe60599ae774429`  
		Last Modified: Tue, 26 May 2026 19:11:50 GMT  
		Size: 8.7 MB (8704227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e2e956d7c4a3fa5a72a4e834fc44cc0789cd97d5b8e60bdacdf2727e8660cf`  
		Last Modified: Tue, 26 May 2026 19:11:49 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
