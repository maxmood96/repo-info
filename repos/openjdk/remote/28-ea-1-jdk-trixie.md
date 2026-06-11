## `openjdk:28-ea-1-jdk-trixie`

```console
$ docker pull openjdk@sha256:34996c4637082bbb8098d60fc5da4587606f71f40a3b26e13c409cf42fe724f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-1-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:f2ddf8aa8c607fc78ae6b1dbe4c96d8c148dbce37a598d55b8f3908928df764e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385947671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4a7706fa8c92d739b087cfe3cfc2c81f4217ac25495409f61029e7812ff6ef`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:18:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Thu, 11 Jun 2026 03:18:38 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:18:38 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 03:18:38 GMT
ENV JAVA_VERSION=28-ea+1
# Thu, 11 Jun 2026 03:18:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 11 Jun 2026 03:18:38 GMT
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
	-	`sha256:4f628dc9c8d83960d0c619c3a018c63efc9957782b9db99b3716b50d4ffec228`  
		Last Modified: Thu, 11 Jun 2026 03:18:18 GMT  
		Size: 16.1 MB (16065645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e838e04feaa710d2cbe5552e838560d6a538197d009f4605c4d0ef883c379b20`  
		Last Modified: Thu, 11 Jun 2026 03:19:05 GMT  
		Size: 227.1 MB (227144987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-1-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:a27140d59d280072789bb1b3e6247bd6c8b00c9062dcfa33d08de20f95618877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8526779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d279b33d491e52a20c84586d3311a44f67d34bbe337c5e88de55a1fbbfdeda`

```dockerfile
```

-	Layers:
	-	`sha256:b8ff68769985e194c1ec8e89c8e4b38f4ada18e11838f82225914e7621a2b64a`  
		Last Modified: Thu, 11 Jun 2026 03:19:01 GMT  
		Size: 8.5 MB (8508883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f83833290d6d8adcfd69360e792b66bca38d478c1001851c5d58fb0a8626a819`  
		Last Modified: Thu, 11 Jun 2026 03:19:00 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-1-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9ea83d66d2ab000e423178f6faee5797781ce7c7d0c9f88c8d6e9b2d034ade2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.5 MB (383490470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c74d195a71bb1c3ed92cbeb70f2b4db612e55892b6894803c587555b8e5979`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:18:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:18:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Thu, 11 Jun 2026 03:18:50 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:18:50 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 03:18:50 GMT
ENV JAVA_VERSION=28-ea+1
# Thu, 11 Jun 2026 03:18:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 11 Jun 2026 03:18:50 GMT
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
	-	`sha256:3e0104a7a6f0bb87d6ef1d5b06fb7d319e3e8d88f2ff6717577f0124ff73ed20`  
		Last Modified: Thu, 11 Jun 2026 03:19:15 GMT  
		Size: 16.1 MB (16071341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2caa7f31af8b492b20680a306e4044820d5c72a45d89b3d720f9017790721793`  
		Last Modified: Thu, 11 Jun 2026 03:19:20 GMT  
		Size: 225.1 MB (225114115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-1-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:6b541f7187573bac110b4724354d11e4480b9f7b6a30fc2ab7e31d6d4c915d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8721051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb2d0736b2791cc9ffd09df4f08d8b44e02d4c8e1ab7d0905dc2406922f1781`

```dockerfile
```

-	Layers:
	-	`sha256:716f71849d2219b6ab786c393e931b50db0c5aa698b97885aa660194c9785785`  
		Last Modified: Thu, 11 Jun 2026 03:19:15 GMT  
		Size: 8.7 MB (8703036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eeef5041fcc6b23ade92439144f6c465e5530dec2a308707ca2cd76966720278`  
		Last Modified: Thu, 11 Jun 2026 03:19:15 GMT  
		Size: 18.0 KB (18015 bytes)  
		MIME: application/vnd.in-toto+json
