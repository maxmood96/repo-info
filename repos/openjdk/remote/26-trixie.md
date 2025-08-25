## `openjdk:26-trixie`

```console
$ docker pull openjdk@sha256:8efc676996f6f3305b2618144da26d5c85c4d6068db17dd5a7e1ef715f38d575
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:3338d349e51c70b245ed8779aab79015a84e0cc8ce4790f05d387c3d51e758ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381933731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d1af935502074d3ee9942b8319ae476fabdba83015fa652f64a95c1972288c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:8634cdfc805e8d8d5ad51dbbd93a8f205975bbf6218c33e401a81d56a669b83f`  
		Last Modified: Mon, 25 Aug 2025 20:56:24 GMT  
		Size: 16.1 MB (16061334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccef4705f61cc8b6afdf5d05fc5a95a1f53b5abd84f50fc85f33970fbf47f7f`  
		Last Modified: Mon, 25 Aug 2025 21:44:41 GMT  
		Size: 223.2 MB (223203861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:30055cc601c5660ef426c6d28b8fd350852970982927ef0f447697e8b8e5a9a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8526931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3bac0a07053db4194176d0ebbe781ae81d705af7608fa1daf8d1519ddee919`

```dockerfile
```

-	Layers:
	-	`sha256:06a3434fef8d5aebc0699b5a2b22a2bea27072d5e90db56fb0cf9cc928bda7a4`  
		Last Modified: Mon, 25 Aug 2025 21:24:20 GMT  
		Size: 8.5 MB (8508348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b904e84a9d612a71f470033971e0b10e682be25916d859e82f147b88cbe0a09`  
		Last Modified: Mon, 25 Aug 2025 21:24:21 GMT  
		Size: 18.6 KB (18583 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2cc0b45c7a9513d0aa6a2fbd8531186379cfcfbec5000aff2ab15e23f47466e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.3 MB (379311796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18521e20df04e1855038d1ac3425b484a28cdaed4de9f1d78b32c8017772492`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 16 Aug 2025 00:56:10 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:56:10 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:56:10 GMT
ENV JAVA_VERSION=26-ea+11
# Sat, 16 Aug 2025 00:56:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='f37dba6a92e49b69b66df52a6eaadbd068ae8630d3074ca93bd6ebfa8f6e5ad9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='66798fb794c9b99dd02997b58459ecd7100f79760643ca7fc68cf2303a20b085'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:56:10 GMT
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
	-	`sha256:e1128f5e5f15e4f083eb09039d869e484fcdd45b2bdaa86b7fc51cd6f958e31d`  
		Last Modified: Tue, 19 Aug 2025 00:48:41 GMT  
		Size: 221.0 MB (220991352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:97efe2bab49b0f67292b15dc987a79a9bccdcd3706387748fec8fe10efe87073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8721889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca0870e7d9a3e7859381367098f7480a6cc9c2cbf06219e8246fff1462d5f1e`

```dockerfile
```

-	Layers:
	-	`sha256:e6917dfa949711d42b318a0d6f4f8ebc5dac3dca0c4201fa6844b407cfe8d22a`  
		Last Modified: Tue, 19 Aug 2025 00:25:01 GMT  
		Size: 8.7 MB (8703162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d2deb473769a5782cea70ba3feaa2e85f42c5c96184b85c86674d1856500c7e`  
		Last Modified: Tue, 19 Aug 2025 00:25:02 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.in-toto+json
