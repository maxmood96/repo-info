## `openjdk:25-slim-bullseye`

```console
$ docker pull openjdk@sha256:13e4739a5b7eb64cf78f05f57ed4b042440cdab4b3318208327c3859ebf36bbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:81dc30d84d3783857cc21dfecbef1ddccc34494daf86a050622d13ca4713c25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244703470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f13fc2c857bdad39eda68c3d3d7f40c389ca424de94f9254944fbc118c5777f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Jan 2025 07:52:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 10 Jan 2025 07:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_VERSION=25-ea+5
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b4ee63f91536c06f46e6f0d9c45e820bc2cb552046df27aa5c77d0bacc35aa21'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='43d1f9c863580d839b21121bc0c09ef0525d80ce1a3fbe26ea22fe2d77eadf7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5d0ee3db0fcdae6b6090f048c8329e3516b49a8eac140f95ed212a9333ea6a`  
		Last Modified: Tue, 14 Jan 2025 21:50:33 GMT  
		Size: 1.4 MB (1377242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8025acab58a6dc601897541d9f60ac691a32e5cbf63f293536b22922fa3a67df`  
		Last Modified: Tue, 14 Jan 2025 21:50:59 GMT  
		Size: 213.1 MB (213073563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:d80cf0abdccc2ae052d6651625111a6ab3b1a63a08fcec65fc274a7523d53611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b27df3fe2e2725e3920aad0dbdacc7c3b1ee2f835d6db44a3788c49347c86a`

```dockerfile
```

-	Layers:
	-	`sha256:526e72b2da918b4fc56944fea08f1471557a43dbb2474384fd59cc7de54e13ea`  
		Last Modified: Tue, 14 Jan 2025 02:36:38 GMT  
		Size: 2.8 MB (2827914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65712d62ca525596af0cbfc1054102fb3c4c3c5d5d11c7dc6e081466f5a216ca`  
		Last Modified: Tue, 14 Jan 2025 02:36:38 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4755fb5f1e82a30e9e4710f1aa0b41a874e67cb70bede49efaf5a6986c281495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241141710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42490452a3dc8c82d10e2562fa249119875c3b107afbc61c06ba515b1d35c18`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Jan 2025 07:52:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 10 Jan 2025 07:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_VERSION=25-ea+5
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b4ee63f91536c06f46e6f0d9c45e820bc2cb552046df27aa5c77d0bacc35aa21'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='43d1f9c863580d839b21121bc0c09ef0525d80ce1a3fbe26ea22fe2d77eadf7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1401c2185a5f6b10d74a84de713de9f232aa9ed5f90f55098b0de741737421d6`  
		Last Modified: Tue, 14 Jan 2025 07:44:51 GMT  
		Size: 1.4 MB (1361281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2f22021405ca10a8edbe5de5d1dae83fc662085b8b1957663614b9f8bd7a43`  
		Last Modified: Tue, 14 Jan 2025 07:44:56 GMT  
		Size: 211.0 MB (211035516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:69c280e9c39fda507d087fd00540a562020c3ac428a46b916a52c83a59162022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ed0a92e7367cff7564e324a4e05770424635b234baaa2ab3a052002af0e38f`

```dockerfile
```

-	Layers:
	-	`sha256:2345e4b7c7b26cf5e13329fd25322f4f45f04619f9c8a7c823fb2834679a7fee`  
		Last Modified: Tue, 14 Jan 2025 07:44:51 GMT  
		Size: 2.8 MB (2827566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad4b1814f448ed911fff6db51a482f6a261f07ed1d78da67ab0a37d601afa1b8`  
		Last Modified: Tue, 14 Jan 2025 07:44:51 GMT  
		Size: 17.7 KB (17699 bytes)  
		MIME: application/vnd.in-toto+json
