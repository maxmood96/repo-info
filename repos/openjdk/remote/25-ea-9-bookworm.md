## `openjdk:25-ea-9-bookworm`

```console
$ docker pull openjdk@sha256:2b764619553c67042aaa7c8901c45212734793215ad9f286da6d77dbd2632559
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-9-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:051e3744d0a3d850d6f51e38b15db47fe123c729de25fa424e1390b9c6accf34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.8 MB (365802005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143266fbc2b3676708c3b40555bd4c29d3b24d6f77fd17cd42264853be632a85`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 07 Feb 2025 01:53:06 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:53:06 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_VERSION=25-ea+9
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='7c57d59eebec0a42a9bca9611b79759eaaeee24f115a9503f4977e5f089eca90'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='7297335988877649a1eebd21261a54e3d96e4f82038766b1a8dfae4fc177ea02'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 07:11:25 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 08:41:29 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065f3203ce9c5215a49806dec23077a79c4337bbd02526d1e91b312a00380b3d`  
		Last Modified: Tue, 11 Feb 2025 04:45:55 GMT  
		Size: 16.9 MB (16943045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3ea8f92ffc2bd4c75f9f7c50b09e80873b6263100ad955299e9a2cc504b582`  
		Last Modified: Tue, 11 Feb 2025 04:46:11 GMT  
		Size: 211.9 MB (211926626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-9-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:fe08ceb5962b00d9168ba8252990ad980610e9b4a618522ddf674d5e055482e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8457976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df59cc83e21fe9f8b430388158485261af8c54eefe0a97c1427c3b76a7022951`

```dockerfile
```

-	Layers:
	-	`sha256:59736f19bdf1cefcf0a48963909b52e5ff53e966c3a036513c33384cb92219c5`  
		Last Modified: Tue, 11 Feb 2025 00:28:01 GMT  
		Size: 8.4 MB (8439375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75a0f0b775bc66819cf89f1c9c4b32357e9b2bfcc8ebdf1a91e7710aed51da12`  
		Last Modified: Tue, 11 Feb 2025 00:28:01 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-9-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b48211b44d44ee79d27096c2f8934ecfe462472795f88ff8102caaf372a756bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363886635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447c8bd9c7f20b8eedaecc714eb3277c05ded0ffcfc1fc66c5a167704c4acee4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 07 Feb 2025 01:53:06 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:53:06 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_VERSION=25-ea+9
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='7c57d59eebec0a42a9bca9611b79759eaaeee24f115a9503f4977e5f089eca90'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='7297335988877649a1eebd21261a54e3d96e4f82038766b1a8dfae4fc177ea02'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Wed, 05 Feb 2025 00:14:09 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d3572a68af0b860060b7ea84adfa8406fa20cfd1337c947dfb661aa965eee7`  
		Last Modified: Wed, 05 Feb 2025 02:21:14 GMT  
		Size: 64.4 MB (64357505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67f15c6066247c5954087e18794060d84d9a3a4d17a01ccfd724f83a823d824`  
		Last Modified: Wed, 05 Feb 2025 07:45:45 GMT  
		Size: 17.7 MB (17727283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e753af0c5c877622e5db6588a88e617024e5a5052096e73777c0729fcca6d2b`  
		Last Modified: Tue, 11 Feb 2025 06:51:50 GMT  
		Size: 209.9 MB (209896866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-9-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:150b2bc91d98aadb782b9929af7c0bfa550c00be3bd4569c75f0592d6ff8994b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8594987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c9f39ad5c003cc218a3fe2ab8890ec94dfa439702f2fe923e9007c43caa6fc`

```dockerfile
```

-	Layers:
	-	`sha256:111729bd66fb145346979ef53c859fdc3e6ec3df1db4d4f1541bca152d11a151`  
		Last Modified: Tue, 11 Feb 2025 00:35:52 GMT  
		Size: 8.6 MB (8576243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc6777efe06069ead957f10d257bff7e7a76e9769dd0ae3263e006d59cac9b53`  
		Last Modified: Tue, 11 Feb 2025 00:35:51 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.in-toto+json
