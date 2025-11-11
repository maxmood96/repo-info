## `openjdk:26-ea-jdk-trixie`

```console
$ docker pull openjdk@sha256:7ac7d8d21be8e7bd894ee1408a66f9c5a5d06c5b06747ad084c971a63e68a092
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:32d0d81d763d3ea76ca5dc23811826b6adf1144383bad532dcbeed93fdf42277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.7 MB (384702187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1407661ecc57c6a0ce3ae19aa3e7bf3d2673eabb36b49a3e32eccc062543fbef`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:42:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3143549f2b8b3ad8d79efdc47824641c6771796b3770f3c637a38aabd2b3462`  
		Last Modified: Tue, 04 Nov 2025 04:14:53 GMT  
		Size: 25.6 MB (25615393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e8e93b0d018b135d833207c6feaba205653ac52e0a80d214477ec0de239dee`  
		Last Modified: Tue, 04 Nov 2025 07:43:02 GMT  
		Size: 67.8 MB (67776858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e070463136186b5daf1e4038ab867a507a2f75e6c75dfdf36636f4102c19fa`  
		Last Modified: Mon, 10 Nov 2025 19:53:44 GMT  
		Size: 16.1 MB (16061453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7781e9987dd1b84ec6e15eb3c7ab7951b599268199abec96242cc4b672b3b5`  
		Last Modified: Mon, 10 Nov 2025 22:29:07 GMT  
		Size: 226.0 MB (225962855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:9253b601ec9aa32b6404421be94c6d6f6f30352a760f19b9fd29be91dd3703c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc1e7bfa1e30057ca12f53dcb86f8576e5bb56a21a49bda267498aecedf2a33`

```dockerfile
```

-	Layers:
	-	`sha256:5b2238f7f211c72ba9ca437fea3a56a7b17cdaf5877fc19097efecde29dd7983`  
		Last Modified: Mon, 10 Nov 2025 22:24:25 GMT  
		Size: 8.5 MB (8509895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dca0dd7c27c722e926ee599ad91058addca6eab9441b93e559c5a42f0ec5dd8`  
		Last Modified: Mon, 10 Nov 2025 22:24:26 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:54c12d699d332cb71da35a6bf3affde529f62c4e15715b4df4cf5c86e060d533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.1 MB (382136899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332d107ce850e3f8ef3a4500bedb3f218b4974be4c6c0b7500477e9561abdf0b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 10 Nov 2025 19:52:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:52:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 10 Nov 2025 19:52:57 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:52:57 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 19:52:57 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:52:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='c5cb587a920ddf65225352cf2494965786acd1de8d6748a976d7498d0783a396'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='427f53a6635347b853f695324253b6d78f69cc09334a9cb1031a801e43358883'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 10 Nov 2025 19:52:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f766ef2ec48737a0f300405019c312acd667d14467b50c402750d1454e3591`  
		Last Modified: Tue, 04 Nov 2025 01:30:11 GMT  
		Size: 25.0 MB (25017577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186d0d0b2411f880d1a385216013fead1acb2dee0584aac75da87dfdeb1202db`  
		Last Modified: Tue, 04 Nov 2025 02:21:20 GMT  
		Size: 67.6 MB (67583874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf95487a0e80ccde028d7bafcc00741a2d88b0e60e5227a5987f8a0aa0008ad`  
		Last Modified: Mon, 10 Nov 2025 19:53:36 GMT  
		Size: 16.1 MB (16070718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0575e0062938078775eb104b9293bb490567b5cf2b99db30c61a66e7985e4c7`  
		Last Modified: Mon, 10 Nov 2025 22:50:20 GMT  
		Size: 223.8 MB (223814300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:5341771caf52cd3b37194e0fc654c21ebf1ebd9e40c4ea57f323fa7481533117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30988e6608cf2d1f60c72a428e054d72603cf6ea40dcdcbae6e0a1b1a5c7cd8`

```dockerfile
```

-	Layers:
	-	`sha256:1d6f2707ce2c701b1dbc2cf71e883e1256594ff68dee0a8a13101f5cc3dcd22a`  
		Last Modified: Mon, 10 Nov 2025 22:24:32 GMT  
		Size: 8.7 MB (8704685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03cde89bf64bd1da6c6cfcb06353e26063d1eca4a0450614226721161c42aab4`  
		Last Modified: Mon, 10 Nov 2025 22:24:34 GMT  
		Size: 18.0 KB (18031 bytes)  
		MIME: application/vnd.in-toto+json
