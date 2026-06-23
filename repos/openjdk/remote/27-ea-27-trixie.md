## `openjdk:27-ea-27-trixie`

```console
$ docker pull openjdk@sha256:9fa24a0a4bb577747b674106fddd42bbd72356820f9da99003dc17c6cc7d1dd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-27-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:710f2bcb718b5113f082e5f62cfbf5cead5ac2f040023a250cc9d9fe5c46ff45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385870384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e574b4d79a31359e8f17fda21c0cace2ca6bff3b5ad28c6f77f3626e25c1cf`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 22 Jun 2026 22:37:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:38:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 22 Jun 2026 22:38:00 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:38:00 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:38:00 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:38:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:38:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b365b6ff7b7e310e1b9a88f996e65b89969c7fa450492b68249d1d1c38e0676`  
		Last Modified: Thu, 11 Jun 2026 00:42:51 GMT  
		Size: 25.6 MB (25635173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca884014342f240be01d391b498c3ec61b2f4af2c205e7e9a0b5ac2cb2f24c4`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 67.8 MB (67784745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7076f199d81dfd28b52309c71a1de560f0882f7bdff78414a8286f7d58249a86`  
		Last Modified: Mon, 22 Jun 2026 22:38:23 GMT  
		Size: 16.1 MB (16065742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eff7f2340e8f0158e039db348d03fd20dd8871e4847238c9ca3ecad046f5915`  
		Last Modified: Mon, 22 Jun 2026 22:38:28 GMT  
		Size: 227.1 MB (227067603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-27-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:1883a903daa50bed10266880c8dab9e70b3ccc131e4679be6c7451144a60b7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8526808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ebfa029fd8814f3ecc61858442089efefeac97d3983647aa5dc8ae2388a49c`

```dockerfile
```

-	Layers:
	-	`sha256:a704a7b29fa768d0942287fac014bfa334fe738d46b2471a66c74845850c7b52`  
		Last Modified: Mon, 22 Jun 2026 22:38:24 GMT  
		Size: 8.5 MB (8508895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d47c0415e19889411ada6b0de49041f0b96b8afac7a0ba8afb7495c0b834ce`  
		Last Modified: Mon, 22 Jun 2026 22:38:23 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-27-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5153b55430f9f1209a4796aa8b1cc9980dafb70a3af62b485e5c82658b11a039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.4 MB (383430277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fc8d4fdfecde2b7e9f83d510ecdc4e9231efb8e48d875b677dfc1b30f3f04b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 22 Jun 2026 22:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:37:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 22 Jun 2026 22:37:50 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:37:50 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:37:50 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:37:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:37:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2ab02859108b91c1c26f2badd015b5215eb066b7ef4f3a22bd1536a8debe96`  
		Last Modified: Thu, 11 Jun 2026 00:44:32 GMT  
		Size: 25.0 MB (25026911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2e427d8856f71d8d3667d1c4d9274b8aca2bd9d228387c51c211909e51263f`  
		Last Modified: Thu, 11 Jun 2026 02:22:21 GMT  
		Size: 67.6 MB (67599934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc2245a58afb1dea8ed7eac32f5d1ac862be2bfca72ab5868930318ec6eb4b2`  
		Last Modified: Mon, 22 Jun 2026 22:38:16 GMT  
		Size: 16.1 MB (16071371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0236e7eed99c37ec821d9e0ece36cbf87bfa8e908628e9d63378f7f3aa0f8dd9`  
		Last Modified: Mon, 22 Jun 2026 22:38:23 GMT  
		Size: 225.1 MB (225053892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-27-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:80f88d16a605d0498795c8d5f42b5e1d0388164844d178cfbafbc70dc6ebc572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8721080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13ed56e659f1530c3e6c4905e1d1a608a34dd8be72fa8f184a906396e312517`

```dockerfile
```

-	Layers:
	-	`sha256:440ad81d385b80c94c078b644d216c8aa5e77e8741618bc0478b064a6146c038`  
		Last Modified: Mon, 22 Jun 2026 22:38:16 GMT  
		Size: 8.7 MB (8703048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88fc93df1946493cdc72ba50f60180513847ff20d5a3fd5999d86bf7b8f67e4b`  
		Last Modified: Mon, 22 Jun 2026 22:38:15 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
