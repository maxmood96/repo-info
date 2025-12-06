## `openjdk:26-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:17542e96ad4736812e055af94bbd3fa11e04cceec7eb361ea2f3c1e68924b528
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:76e22d0b411fe2dc8a957ff7f7c2a71045e03b43179ec46d93ce4e621d922e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.8 MB (381783122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aa396d3aa403f5d539953f15743c8625f63d4a5c13ee50cd3fa575fab55e1b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:35:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 06 Dec 2025 00:35:03 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:35:03 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:35:03 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:35:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:35:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078b2eece9b24f617524f986db4dd04f977e3e7d6fe15a9088a584147bc6ba05`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 64.4 MB (64396262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa457f55d708613388aedd90fb36936b6d8c5d3ff6fd86d64b124884725e44ce`  
		Last Modified: Sat, 06 Dec 2025 00:35:39 GMT  
		Size: 16.9 MB (16943701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5ed266848fa40ea4f908ebbcede261eda0ce22eaad3fbf7194c17430d1494b`  
		Last Modified: Sat, 06 Dec 2025 00:35:43 GMT  
		Size: 227.9 MB (227933050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:67757ad0f0514173b84406b710b8cdb74acb84e4f469847d5899a278746dad16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bfb096e5f45dc7ece9aa156673bce380433f4a682fb188805054d69bca2c3d`

```dockerfile
```

-	Layers:
	-	`sha256:1457c37c62864bf734a83927ad763b5de7a67ff80b1faeb15e86aa038811fe8e`  
		Last Modified: Sat, 06 Dec 2025 01:23:43 GMT  
		Size: 8.7 MB (8668200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf2bda4dcca871c058c38792da829ef335d36cbe44163a2ef47f9e4df91b3c69`  
		Last Modified: Sat, 06 Dec 2025 01:23:44 GMT  
		Size: 17.9 KB (17937 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:368690b8f00c477c1b5cf5ce3e2d3956199b17b25e167aee1f766958655879d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.9 MB (379906978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568e96a7a5c0fba1ff57edf0a3e36760475584cef3b7a8a71adf1e74bcf10b4d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:35:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:35:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 06 Dec 2025 00:35:35 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:35:35 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:35:35 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:35:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:35:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d805ffe4d6247a3ab7494e663f6ae84d04e36c5270a200f1d1d34db32a26c`  
		Last Modified: Tue, 18 Nov 2025 05:38:35 GMT  
		Size: 64.4 MB (64371414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ba83d7fe90310fb3a396bb98e31612d525553477f448b9f5c08ce98c176d2d`  
		Last Modified: Sat, 06 Dec 2025 00:36:14 GMT  
		Size: 17.7 MB (17727790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8636c48e48ceecf8643ed8e449aad570c3c5ac1316b2387f70e0a00cb95dc9a5`  
		Last Modified: Sat, 06 Dec 2025 00:38:04 GMT  
		Size: 225.9 MB (225850316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:8a5e96593e18ade108eaf6bcffe8a03c15ccc54fb15bd44df15e35c03b8ab801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f4f40c85fe3520dac358e1c0e5fba163e8b689e9f7064b65eec26ce25d960e`

```dockerfile
```

-	Layers:
	-	`sha256:b627be18a1115da56ff518ee250d7787b296290b9c94cf6adacfa920b48f8649`  
		Last Modified: Sat, 06 Dec 2025 01:23:49 GMT  
		Size: 8.8 MB (8805045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c8b18033a204766bc4b9ee9f2277acbd8812a5911446837bc8233fe837b7e82`  
		Last Modified: Sat, 06 Dec 2025 01:23:50 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
