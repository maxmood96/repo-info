## `openjdk:27-ea-27-bookworm`

```console
$ docker pull openjdk@sha256:92c1429441773f4aa50828e1b6db5026de05bf00c3432ce910e00b166c8a00b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-27-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:409d87998bffab4cf846cfa633c942f639a12fd4cf5a69ce10fbfb3acc8a8426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.0 MB (380963098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74efce44782d585e851eb56146849b7274432b2525ee1a73faf43c4d54c16af4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:38:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:38:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 22 Jun 2026 22:38:12 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:38:12 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:38:12 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:38:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:38:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbaeeb62b9d03a1204b85c3b257aa3e1ce2c4ccfeea479fb2e659211019c29d`  
		Last Modified: Thu, 11 Jun 2026 02:24:43 GMT  
		Size: 64.4 MB (64404116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034894fe5b205d1cc5dd492892fa4c62f73df7040657c9052555a4e5bf0a41f7`  
		Last Modified: Mon, 22 Jun 2026 22:38:37 GMT  
		Size: 16.9 MB (16946459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc555a694cd06fd27ccdd1e587e6ee403e294afa1849ffc30f1947e40ea97bd9`  
		Last Modified: Mon, 22 Jun 2026 22:38:42 GMT  
		Size: 227.1 MB (227066481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-27-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:faf95d094564277827caebda6eb81c54aeb5fcc4d69ddf1c329e88005ea07679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8684313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3ed1bb0d0122e6e765f2e790d57e9b9098bdd17c37f902ce490c9b571b1572`

```dockerfile
```

-	Layers:
	-	`sha256:dbd0a3574afde2a8c930cb1ee3b781c327c80ee17436e347e0db6c3dcc699fae`  
		Last Modified: Mon, 22 Jun 2026 22:38:37 GMT  
		Size: 8.7 MB (8666374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f83947d3d4186bd478b976c04a604fc137b65405a8bb279c1fd59093af404474`  
		Last Modified: Mon, 22 Jun 2026 22:38:36 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-27-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:67caef1ec549c990f331da40d8f6e67bfc5103c9402e12f3d07c71d7bc829cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.3 MB (379269813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0d79cce74c528ea562c6a928c0a6b3caba93043e646b9951ec28eae178a442`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:38:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:38:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 22 Jun 2026 22:38:11 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:38:11 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:38:11 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:38:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='4f81468b39b9f6516ce5e3de3130e404d508be7d77d601ec1217056163ff6a6e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='048e4f60c3069ab86e0a068eedd93e33e62ec275a1b2a9033bb07c925f01b7c9'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:38:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b715a6712db064e97302c819acd7a39c0c72f8a315ff83c6ad1c27bfa1b275e`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 64.5 MB (64487878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b6147783351145c939a3cf27b0ecb4fd14f1bfc97bc9f0f22b3dbf454ce951`  
		Last Modified: Mon, 22 Jun 2026 22:38:38 GMT  
		Size: 17.7 MB (17730391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51de5e8f4ff1b42ac7bf7c1f5b091dd24afd9dafbf9d76acb10e7d59f9d2eac5`  
		Last Modified: Mon, 22 Jun 2026 22:38:44 GMT  
		Size: 225.0 MB (225049232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-27-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ce0f50d8e0f2987cedd771f002941d67d57360b4defb1b971dd548f7cbf34f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8821277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f03593ffada5dacd0a214df324e7f9a88f94abf0b2c9bfa575dd057b265d13`

```dockerfile
```

-	Layers:
	-	`sha256:9c75b06bf1ca33e0e4d1964036af09646f032945ba7573d5051da00dca2b963b`  
		Last Modified: Mon, 22 Jun 2026 22:38:37 GMT  
		Size: 8.8 MB (8803219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e1e107d1b013666ad52b791a43a084ce424b0c82058eee08f1c935ce86de41`  
		Last Modified: Mon, 22 Jun 2026 22:38:36 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
