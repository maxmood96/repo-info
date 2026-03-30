## `openjdk:27-ea-trixie`

```console
$ docker pull openjdk@sha256:ac1d57db7212adffa6067a1fc47092dca6d8f4c3bb8d1f20823be366aa5ee99a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:863dd3aa68a76b3bd5a480bde3ef880548c7d9b8fc818aab23aaef77b3dd698c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.4 MB (387373981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9ece3f9ed10df60266db79720ee2beffdaf101ace2728522dff85eede28a00`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 30 Mar 2026 17:51:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:51:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 30 Mar 2026 17:51:38 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:51:38 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:51:38 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 17:51:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='5cfe1cf2f5d5ebbcdd826c7298fbabc42d656edbe9544c74b1ee84df6e5326a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='ab3f14d81c06590facec1138b71b55a7f64d47c0e0845113c9a8ecd4be6751bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 30 Mar 2026 17:51:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a0e7d77f0c84203cab438fcf345647c8121bbd80506a3c692f8608a14c4f4`  
		Last Modified: Mon, 16 Mar 2026 23:25:57 GMT  
		Size: 67.8 MB (67780758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500d08c60817bd8ac0207e3d201663503a9a77514aa3677daa0d26a59f624f94`  
		Last Modified: Mon, 30 Mar 2026 17:51:59 GMT  
		Size: 16.1 MB (16063976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31724f7a2570294dc434148570bddad95c34e7ac81cc62859228851f5bb6f4ff`  
		Last Modified: Mon, 30 Mar 2026 17:52:04 GMT  
		Size: 228.6 MB (228610002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:7988672bd809a86149a8e29f7badd17d3ae6b2900658e4010b5383c528938526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8529049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6bd84c89c6f01ee991b92150005a5573f6f6d64b6690107c78c7cb6cff80a4`

```dockerfile
```

-	Layers:
	-	`sha256:aa44500cd8d75da5702b661b78f2efe3b065668b51d6e6c5a6e49334725e2848`  
		Last Modified: Mon, 30 Mar 2026 17:51:58 GMT  
		Size: 8.5 MB (8511136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24026b4f490a5b834c0d004dde0a1972a04967d3cf0e56b6e45ea82fda606096`  
		Last Modified: Mon, 30 Mar 2026 17:51:58 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:67a056c2c95ddf15fefe381d3f5a737d01e967665d780d43abf37e9606125987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384919121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4b18ade1400d662679a4e7e965458312eb3a6a82660bb656886c17e57a6da5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 30 Mar 2026 17:49:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:49:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 30 Mar 2026 17:49:18 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:49:18 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:49:18 GMT
ENV JAVA_VERSION=27-ea+15
# Mon, 30 Mar 2026 17:49:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='5cfe1cf2f5d5ebbcdd826c7298fbabc42d656edbe9544c74b1ee84df6e5326a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/15/GPL/openjdk-27-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='ab3f14d81c06590facec1138b71b55a7f64d47c0e0845113c9a8ecd4be6751bb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 30 Mar 2026 17:49:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16813bdedcf0a1acbd78336c5bed6fbfaee2674574408140ba7e896cd49cb95`  
		Last Modified: Mon, 16 Mar 2026 23:31:00 GMT  
		Size: 67.6 MB (67584568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d539934661406b0b78c2a32fc18a4ed29ea04c98082daffbdcbbe10f5d61593`  
		Last Modified: Mon, 30 Mar 2026 17:49:44 GMT  
		Size: 16.1 MB (16071531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cca3897433def527cedb74f2fd73014d4136fbc501e085f8a72f85c78a89e1e`  
		Last Modified: Mon, 30 Mar 2026 17:49:48 GMT  
		Size: 226.6 MB (226574341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:20428b240f4ce7fd8678760b5d9fddad6cd16da3123d4dabc528104f37512ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05ed52f204be148c0fa7f0fc489483c1caa13d685da3d61c04195c653a5d2fc`

```dockerfile
```

-	Layers:
	-	`sha256:f0e36802c4e2bf750b27cd9fcbf0d3aba3ff5609e07cf855791235d0b781352a`  
		Last Modified: Mon, 30 Mar 2026 17:49:43 GMT  
		Size: 8.7 MB (8705926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96fef3472860ad9bad93875854f763c0c2f7edc362ca8de04b06377f5bee0ea9`  
		Last Modified: Mon, 30 Mar 2026 17:49:43 GMT  
		Size: 18.0 KB (18031 bytes)  
		MIME: application/vnd.in-toto+json
