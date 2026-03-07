## `openjdk:27-ea-jdk-trixie`

```console
$ docker pull openjdk@sha256:21efa08f20057f297da452dade632ee8bcfe252f2fb7acaddafe7e3ef934f2fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:2eacba5744ce104084d134abfc3c14c949e354288d2a79492876a4120fca9c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.3 MB (387291591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4249fd86532dd94368acbac8d1b76e45bf281dfdcbc070e14b64d54eb7cf84b4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 07 Mar 2026 00:41:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:41:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 07 Mar 2026 00:41:24 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Mar 2026 00:41:24 GMT
ENV LANG=C.UTF-8
# Sat, 07 Mar 2026 00:41:24 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:41:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Mar 2026 00:41:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed881fbf1b07b42dd470cd5b56a8feb684d60879c6f8028a9e7a8715e0e72361`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 25.6 MB (25614562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da421ddeb655bdfb3960e490b39373b0d1351e3eaba61d01978107920638392`  
		Last Modified: Tue, 24 Feb 2026 20:04:27 GMT  
		Size: 67.8 MB (67778971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb728b28b4afb8995853be49a79519e9d654b7065d5433c3ff54c1ebfe17fcb`  
		Last Modified: Sat, 07 Mar 2026 00:41:47 GMT  
		Size: 16.1 MB (16062990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90c6d34f8f8139db9bb9067391bed563b84025c79254b2d59f0b33436657484`  
		Last Modified: Sat, 07 Mar 2026 00:41:52 GMT  
		Size: 228.5 MB (228541944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:a28d91ec37e2d86edf276f7e745310dc3aa8903b3c6f7649b74102f332575b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8528939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7358c563dc734bf2e01fda3233761029fde941b3017ca0f9771b14986218f77b`

```dockerfile
```

-	Layers:
	-	`sha256:9ed82fd522653b370f373d2527075e2ad62286aee6c1083a7aa437772239e9f1`  
		Last Modified: Sat, 07 Mar 2026 00:41:47 GMT  
		Size: 8.5 MB (8511026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314f9cdff53bad7cf1bfe6e76f45b03aa0c346035353c676b5cc5779e5182e4e`  
		Last Modified: Sat, 07 Mar 2026 00:41:47 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a7b53b3b5dc5bb2fbb26404ca8edcd4abf3431b17cf04f581215a05338c9e0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.8 MB (384822394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8f4985a59214981699d889ee72215b2113372b15a00084339a27332f0ba975`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 07 Mar 2026 00:42:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:42:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 07 Mar 2026 00:42:31 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Mar 2026 00:42:31 GMT
ENV LANG=C.UTF-8
# Sat, 07 Mar 2026 00:42:31 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:42:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Mar 2026 00:42:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da832d1713c4ed161275cd40c4161680fbdd97c6faf23e71654d26bb2e58d6`  
		Last Modified: Tue, 24 Feb 2026 19:25:09 GMT  
		Size: 25.0 MB (25023493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c46eec5989abc098640d80ee9b97658d4487864f3268219dadc63c0a047866`  
		Last Modified: Tue, 24 Feb 2026 20:15:09 GMT  
		Size: 67.6 MB (67585551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1017518135ff1ba7c4f2d9866b009959b65249aee16760e9f2c1a4606c238e`  
		Last Modified: Sat, 07 Mar 2026 00:42:57 GMT  
		Size: 16.1 MB (16071681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0458a57c6f4de32e1851eebbf908ea2ef1484c8887e04416b9088c362050b6b`  
		Last Modified: Sat, 07 Mar 2026 00:43:01 GMT  
		Size: 226.5 MB (226489501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:8a1633e931647bec7a81e86edab8678e9cb1abb0ea31e9b1c453e8ec25016415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b5a122997dbb162d87add717c88fef9a36a71682a11cecb488dbf787d984b7`

```dockerfile
```

-	Layers:
	-	`sha256:410d3ccb02fc1205c1909d1092b9fa955429d19ecdbcba98095756d36750aa64`  
		Last Modified: Sat, 07 Mar 2026 00:42:57 GMT  
		Size: 8.7 MB (8705816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2e1e66d5a838a0a380afc846db0568c9aa7232fa057bb3bdd096a691960add1`  
		Last Modified: Sat, 07 Mar 2026 00:42:56 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
