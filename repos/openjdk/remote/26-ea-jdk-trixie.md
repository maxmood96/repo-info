## `openjdk:26-ea-jdk-trixie`

```console
$ docker pull openjdk@sha256:72b7e97bc789eb69c3dce77f6739ce4e0789194d57a40d572ecc54348e8dbe89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:c4772294d014e4f7ad780dab465d796597779e5d7cdf58c1980f6823f7a91efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381887677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e9c71f512603163a47e3dd6d31e8659fdb0e42a9b8b86e48ecce5cdb8137a4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:264cc3701dbc662b163be406d0a977305fb2b104b519d075a0eb4bdaa597e148`  
		Last Modified: Mon, 18 Aug 2025 18:16:42 GMT  
		Size: 16.1 MB (16061397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240435cf1617823f43169ec5f2c5a5c955a6536537ee1dcd30c5e208ce4aefd7`  
		Last Modified: Mon, 18 Aug 2025 21:37:26 GMT  
		Size: 223.2 MB (223157744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:b0a7e88522d55a5f591c50ea3a515e0ecccf88545683f693c6e234d7149eae7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8526932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95525a76e96c395b8110c259262e3a4b53062991c8d54b54df7b9f48b320c772`

```dockerfile
```

-	Layers:
	-	`sha256:d9ea69a2b2add88d2e7ba55932fbf1c167d82c06eec8aed8c2e9c1836f93d167`  
		Last Modified: Mon, 18 Aug 2025 21:25:21 GMT  
		Size: 8.5 MB (8508348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b666f3aa32ea3e105d0927bcfa1dc59685dce4909be159eda7a6462a577c4d91`  
		Last Modified: Mon, 18 Aug 2025 21:25:22 GMT  
		Size: 18.6 KB (18584 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-trixie` - linux; arm64 variant v8

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

### `openjdk:26-ea-jdk-trixie` - unknown; unknown

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
