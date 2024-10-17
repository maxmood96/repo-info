## `openjdk:24-bullseye`

```console
$ docker pull openjdk@sha256:fdd8a90b992f4dfc3377d05cf0177bcd4646e705400210152fe3b53b2da86cba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:ea5030266c06e7bedd68bacb6fcdb0dc722680a700d4d0a147c67c0d0b53081d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (351996002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea6d42768cd79eeb72940f1659eb9fc9f097854f2b140341fb7dbd44e1d6387`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 00:48:11 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 11 Oct 2024 00:48:11 GMT
CMD ["bash"]
# Fri, 11 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06817e07ed0f03c17ad0a7aa8ef22b2a6fcf2b939d6212ab0861571ef18a45b`  
		Last Modified: Thu, 17 Oct 2024 01:10:51 GMT  
		Size: 15.8 MB (15764889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173ffc78585eeabe33105e00a7be99b0cad17d5e6edebf7f760d7824fa76969`  
		Last Modified: Thu, 17 Oct 2024 01:11:06 GMT  
		Size: 54.7 MB (54723650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd33b0f7413b7eb69f25852056b042948051496c1e5f92c849bc56ab6655525`  
		Last Modified: Thu, 17 Oct 2024 03:00:18 GMT  
		Size: 14.1 MB (14071378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04412dc01084b18618d4aeeb340125e746022876da5f06fd0662637213df070a`  
		Last Modified: Thu, 17 Oct 2024 03:00:23 GMT  
		Size: 212.4 MB (212355474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:f87d4ae885744160c8757b6884d5f3506a7d63cb9406bf4f3ee0b7408d1654be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8351122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ff5f71c3d24c4c0a2bd53d84da8d3a2e80850f8aaa7da682bf75b0aa546a44`

```dockerfile
```

-	Layers:
	-	`sha256:855b6ee4cf395f28ee95e14dca06ce463e2feae287ecd0edf5ef1f441f89b1d9`  
		Last Modified: Thu, 17 Oct 2024 03:00:18 GMT  
		Size: 8.3 MB (8332621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d6d90fa9f121ec26f1601678a6fc2b3d1d15ea0d997ae54cea6cb916f86f4b1`  
		Last Modified: Thu, 17 Oct 2024 03:00:17 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:da353aea2d4fa6b1b0d2e0fc35ec54bb8efa79eb7202ff4f2a36b529f00e6b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350086969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16a37ac7ed34aa59c44abb9be43e0864488e2d131d0aee0574562b1fa207359`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:20:16 GMT
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
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f212bcfdd3a473cde2991df3e1cf5373d8f097a630557a35fa77d891acce93d6`  
		Last Modified: Fri, 27 Sep 2024 05:26:04 GMT  
		Size: 54.8 MB (54834694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa1ce92c7bed6ff2a4cee6f65836980466a3238b534f95fffecfde74c3aadfe`  
		Last Modified: Fri, 11 Oct 2024 19:29:04 GMT  
		Size: 15.5 MB (15526312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e8aa1ed0c5f93cfec47f441fdb3149cd5527a7fc580eab08ddb7c2c358add1`  
		Last Modified: Fri, 11 Oct 2024 19:29:09 GMT  
		Size: 210.2 MB (210242401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:16b7dc9c25f56a918146e5be4e333a28729b32001430be557cc2f1ac9eadb3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8451594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812f6d42a78bc187158b244a902dbf5d99b64af40bb04795eb3af444bc98b8ea`

```dockerfile
```

-	Layers:
	-	`sha256:e0bce7c3829af6d7bec5c5f9729613665aee1868b45f8372a1c17b4137b8f585`  
		Last Modified: Fri, 11 Oct 2024 19:29:04 GMT  
		Size: 8.4 MB (8432956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dec374074cb2c899bfc97dafcfb40a8974e9b2db90ed109c10375f734ade2430`  
		Last Modified: Fri, 11 Oct 2024 19:29:03 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json
