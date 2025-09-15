## `openjdk:26-ea-trixie`

```console
$ docker pull openjdk@sha256:6e42d2ee88416ad02ff86688e6e51fcce3845e0371e255c52f83c02837c1de01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:350023eb3c730db7897cc855dd8db0e43e52927c22371754ba31f571e8fe3dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 MB (382162386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8337062b7414f63ac3be8fdb4446af51bcd37ce810f72601567ddd8a1f3edc47`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 12 Sep 2025 18:48:17 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 18:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_VERSION=26-ea+15
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='d8fa7cffcc38d68ed218fa285958e163c48a9b0d5c968c0c8859cc0a36e0baa0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='955e3af91d63b89cb5eecc00503ca439d96a9d2cf645e38e4079ed65c5486ff2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22718812f617084a0c5e539e02723b75bf79ea2a589430f820efcbb07f45b91b`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 25.6 MB (25613635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401a98f7495bee3e8e6943da9f52f0ab1043c43eb1d107a3817fc2a4b916be97`  
		Last Modified: Mon, 08 Sep 2025 22:13:47 GMT  
		Size: 67.8 MB (67776756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1111cb52652b35cef7cf393cc121fe80085a2f86958e4efb881cd0390e4ce3`  
		Last Modified: Mon, 15 Sep 2025 16:58:06 GMT  
		Size: 16.1 MB (16061487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c3f2eae4567425c4ea24af99459e1bd5306217b951f93008fdbad51bbb3032`  
		Last Modified: Mon, 15 Sep 2025 18:37:25 GMT  
		Size: 223.4 MB (223430977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:9675289e8ccdfa0bc8563f2cc60fa88a21f9cd1d5daed78786c0fa1d10ce8141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8531556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df4c9b458f2eff955129930ff070842ec6f8979aae75aefaed2a0b1987fe5b7`

```dockerfile
```

-	Layers:
	-	`sha256:5a5c3401aa6d76e33288fc549e0558c1f13d7120b04dd3677befb77c922ff4fd`  
		Last Modified: Mon, 15 Sep 2025 18:24:56 GMT  
		Size: 8.5 MB (8512972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283e36b9d0f2eb0e4cf44c7b479abd12ec357fed2b149ab738e4ded0e9478fd4`  
		Last Modified: Mon, 15 Sep 2025 18:24:57 GMT  
		Size: 18.6 KB (18584 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:794335db3d3eca26542c839783fe46f2441aedd76d11ce67a2450c19ba257f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 MB (379596737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbeffd93c7ae0e0064f4aea0240b872f540de71f18d38bf299856f21ce90888`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 12 Sep 2025 18:48:17 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 18:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_VERSION=26-ea+15
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='d8fa7cffcc38d68ed218fa285958e163c48a9b0d5c968c0c8859cc0a36e0baa0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='955e3af91d63b89cb5eecc00503ca439d96a9d2cf645e38e4079ed65c5486ff2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd36c08acb8bfd3ecaef97bc215303e9b1c59f47cb418c4692d97f29cb1b17c`  
		Last Modified: Mon, 08 Sep 2025 22:26:04 GMT  
		Size: 25.0 MB (25015321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fd600967e6c49c98883d12d3ca7ba50395f75eb436373e95780141122745a6`  
		Last Modified: Tue, 09 Sep 2025 02:13:16 GMT  
		Size: 67.6 MB (67583121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90b13b2ad321a60b60b1cc482e2bc8475731882c9d77b5c3bf7fce24c7a5339`  
		Last Modified: Mon, 15 Sep 2025 16:57:57 GMT  
		Size: 16.1 MB (16070637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4943188092fb9cf8d04c4d352584248b445605ccc523ad094fdf575d5b7729b`  
		Last Modified: Mon, 15 Sep 2025 18:41:08 GMT  
		Size: 221.3 MB (221283912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:796adb370a87c88ca88178a5292365cef2cc9c43c8299a96191e303365e25f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8726513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab926b74a2aba2cb547cf7f3a7cd473f30056d7852183500167fac377ba7ddc4`

```dockerfile
```

-	Layers:
	-	`sha256:db2ed8eab1bbb89e910129c4c999b5dbde8ab173edfcd1ed1156ce54a8106b97`  
		Last Modified: Mon, 15 Sep 2025 18:25:04 GMT  
		Size: 8.7 MB (8707786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fd0ebf5133f4f0758e1bd51d0a5db59088db36dfd83aaa3e6a059ad564bad2`  
		Last Modified: Mon, 15 Sep 2025 18:25:05 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.in-toto+json
