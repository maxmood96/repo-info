## `openjdk:24-bookworm`

```console
$ docker pull openjdk@sha256:9bc9c16a6cdc5165003d360e8b50d39f8482ec639b66c2221ec6ef76342affd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:c3eac0e3155f63bb69e494ee250ae6f83598807b15c7478a6d004b4ab66c7483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.5 MB (367481198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1177d7bceafbc90d1ab7dca124f03854160f1d408ac10e3fe785c868b4e536b4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 18 Oct 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 18 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+20
# Fri, 18 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/20/GPL/openjdk-24-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='b7a84616949bac4a00a9a96d771f6595e7fed371c0a5a54139285311e4c0b367'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/20/GPL/openjdk-24-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='4fe26b4900462d35fcaa9c7b551fd23791906f05eab3a609de8d771cc15ad9d0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 18 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc9ead12b54826e53e15bdda2357191fa94d8842198630c6f45ffca0d59b0e5`  
		Last Modified: Sat, 19 Oct 2024 02:54:41 GMT  
		Size: 16.9 MB (16943003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37cf34ced3af7b701960831d4efce5717f59b8675dda5e69ae29267e55642d8`  
		Last Modified: Sat, 19 Oct 2024 02:54:43 GMT  
		Size: 212.5 MB (212542091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:9cb65734659e637115407b93c44d92295de5866e1c2c527b570d0685efff586d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8445653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a352357a1378fb0857128d31f0b879f74a39c76b612db50a0e45aabd7c2a967`

```dockerfile
```

-	Layers:
	-	`sha256:9f929153286ab614766cc703582ca71302fd24c390f60fb66d6328c2197ee972`  
		Last Modified: Sat, 19 Oct 2024 02:54:41 GMT  
		Size: 8.4 MB (8427035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d085e453aa664ae98ab75df63ec48dd408288fd75e0f2824d3b4b06425acd74f`  
		Last Modified: Sat, 19 Oct 2024 02:54:40 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d80134ebe73a2f6e1df07bd14e47a6b318de91e104936ba70b0ac4a57f578f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.5 MB (365505737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361418eeb963bf9d8beff7ccfa455f61708055c6f0f3bf7bd69bb8b024b709cd`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 00:48:11 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Fri, 11 Oct 2024 00:48:11 GMT
CMD ["bash"]
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 11 Oct 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 11 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+19
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='b283aeaeda2e1fb83a01a61a370e2e95e217a00aa3a51641d1b65244b60b05f6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/19/GPL/openjdk-24-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='1f125899b06296b1948e650bece4c424c5ac572793c9446bac6f39c68a4545fd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 11 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f71cf1903685ed3f6314161e121602758f809a760d2bd2293f7cd8ce1abe1`  
		Last Modified: Thu, 17 Oct 2024 04:36:08 GMT  
		Size: 23.6 MB (23594190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143d0f027108dead9d56047ebcddbf6b5ce9a7d51ab49ac1eeef8590e7bd9764`  
		Last Modified: Thu, 17 Oct 2024 04:36:24 GMT  
		Size: 64.3 MB (64349510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990a792a9a2115a21fb3ba9b030d4a3e6f2c1ce88ed4e8d5298f346907a77eb3`  
		Last Modified: Thu, 17 Oct 2024 22:02:34 GMT  
		Size: 17.7 MB (17727129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844b2f9e9bd36ab5ebaaab2f82171a57257feb3a6ff1e449d6083b62d00b26ae`  
		Last Modified: Thu, 17 Oct 2024 22:02:40 GMT  
		Size: 210.2 MB (210249930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:562e9fbfd15e6b3b428aa2b3563090566ea766c0a5a713f7341e489258e0cfa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8558566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30c2062897eea463ca0c3785336780f4a8cabb9e89a8c98ab6ca94252b99154`

```dockerfile
```

-	Layers:
	-	`sha256:551894cc2988ca2813238d9cc00d2a289a47ae2599bd4e30f2e3c1241ddf7d6d`  
		Last Modified: Thu, 17 Oct 2024 22:02:34 GMT  
		Size: 8.5 MB (8539928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da1ace5c0f06c8cfa62077d23ea31e06ab4e69e71e842ccbe7642aaeb3d02905`  
		Last Modified: Thu, 17 Oct 2024 22:02:33 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json
