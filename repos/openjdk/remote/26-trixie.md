## `openjdk:26-trixie`

```console
$ docker pull openjdk@sha256:83bedcd6a84e58c9164919c83f2f0d1aad6046a2f59bbc8c852dccb2ee91fdaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:59a8acd492d621970988c90592facb9317d2c1c5f3b446754b3ada26ece4cf5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.0 MB (382030311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810428a6029ca8a4cc3fc372e9c51993001424b19e120b986cac7d4f2764e220`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 30 Aug 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Aug 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+13
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bf1fc270d7d30fdafbb1df8cb75b7b9a0e40adba8b72e9655410df7d7475ecc0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='e0d0ccf09df66d71738ff9ba2a927e4169f52d99569f57a346797b83e2dea920'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e4db86de6eba33869491caa7946b80dd71c255f1940e96a9f755cc2b1f3829`  
		Last Modified: Tue, 12 Aug 2025 22:14:12 GMT  
		Size: 25.6 MB (25612940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea45766c6449310ca2fc621a7e00bedb4b9b803a7fbfe2607efce6d2e07e435`  
		Last Modified: Tue, 12 Aug 2025 22:15:03 GMT  
		Size: 67.8 MB (67777316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb685511151120fcf1dda51654b6175ea908d164e83752dbd0b1a7e563ca3e41`  
		Last Modified: Tue, 02 Sep 2025 17:24:07 GMT  
		Size: 16.1 MB (16061210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433d764f1340f8dadbf3cff54f541dd8d80e736a62e8f0e812c06e9044c63600`  
		Last Modified: Tue, 02 Sep 2025 18:06:23 GMT  
		Size: 223.3 MB (223300565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:314605f53ea810b454357865c4aac2fe96382cea47f08618c8041875c822b021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8526932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a8e370425c2ea1e68cea676f413a100278e72c475d7541ace4c05ee5448145`

```dockerfile
```

-	Layers:
	-	`sha256:a304b8e61dbc1f7317bb59f0f4c310a1a995e795a9e59d7dad72e0c59fed7cf2`  
		Last Modified: Tue, 02 Sep 2025 18:24:25 GMT  
		Size: 8.5 MB (8508348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7f17c4857fe960e38bd94bc2764675c528f0b2d75d0fb151304c2cc35bbbc7`  
		Last Modified: Tue, 02 Sep 2025 18:24:26 GMT  
		Size: 18.6 KB (18584 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8032d2c6e52e619e50b673c2531406c7dec1075bc1c999b8bc83308fe8ed7feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.4 MB (379409709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f965e964d493dd63a0b06ea69411c4a87702e94148306476f72b67a7267998`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 23 Aug 2025 00:48:14 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 00:48:14 GMT
ENV LANG=C.UTF-8
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_VERSION=26-ea+12
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='2d6177e017ca138d8990643910b989990751db9370cd78dfc51e5116411e7f6f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='b4e0c4bb252fe005ad3a46c54264e226c554fe95edcbdc9df81dbc268901c7cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923852056eb09462c3344515191318e7aa33ff28057c946bc41a414ee57df0b`  
		Last Modified: Wed, 13 Aug 2025 07:30:07 GMT  
		Size: 25.0 MB (25014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc8bff74cbeacbac9c6869b6a9def273b93cc67de196b347688de2a9185de0`  
		Last Modified: Wed, 13 Aug 2025 15:31:50 GMT  
		Size: 67.6 MB (67593628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e07437b7d82281aa4925b53bf361031ee6dcd0a4c9dc36ebd8b5e912feabc18`  
		Last Modified: Mon, 18 Aug 2025 22:23:06 GMT  
		Size: 16.1 MB (16070603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb954ba7ecac907f1a50f03b4d9647e9b48fc280709a7dc4cb80904bfcf1d20`  
		Last Modified: Mon, 25 Aug 2025 22:14:53 GMT  
		Size: 221.1 MB (221089265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:0bbafb2237bb58caa4a12da34f49aff87c9043de6f485672a5d424ac2fea6dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8721889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b751aaa70f3d500bdce633c93e1a210f8aa911e9a37ddee2c6d69ccca826400`

```dockerfile
```

-	Layers:
	-	`sha256:dee9203acb9bdb82aad01e8ef64bdeb4ce02959f532e3b724205000d4abe61b2`  
		Last Modified: Tue, 26 Aug 2025 00:24:29 GMT  
		Size: 8.7 MB (8703162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a4b2613235cdd9f3f23009748e9ec80a15c63cbb342f73ef103d47e5d3771fe`  
		Last Modified: Tue, 26 Aug 2025 00:24:30 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.in-toto+json
