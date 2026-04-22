## `openjdk:27-ea-18-bookworm`

```console
$ docker pull openjdk@sha256:a5149d1feb122e4c6bfe88639618f540e2e7de57047e4990c4c8e30ffdc936db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-18-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:10e5b84a9c640461bbe1419608c840e08cb7a29880bd377c72777e7a0879f810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.6 MB (382615645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8ff4dce2fecd67355e051efac26cceb53d9f2ddf001e4a7f3b150bb5b02d1e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:41:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 17:41:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 20 Apr 2026 17:41:20 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 17:41:20 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 17:41:20 GMT
ENV JAVA_VERSION=27-ea+18
# Mon, 20 Apr 2026 17:41:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Apr 2026 17:41:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de73ef470b7b271fede6f98a4c8376971bd059ce04ebc13b9f86e34e534b89ae`  
		Last Modified: Tue, 07 Apr 2026 02:43:01 GMT  
		Size: 64.4 MB (64396012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0336c118bd361f9e0448e65fb1385dc4e6aebc2de59b53ddf496aadbad05867b`  
		Last Modified: Mon, 20 Apr 2026 17:41:46 GMT  
		Size: 16.9 MB (16946010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383a469c10d918ff52d38ee7b865b6c424a03356523de08fa86be9c3a6969f70`  
		Last Modified: Mon, 20 Apr 2026 17:41:51 GMT  
		Size: 228.7 MB (228746531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-18-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:cffe6a7b84e8bbda032348b6885f278e8e82610258b3c58ec484f35333d21a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8685556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fd74bac924b574d7f03580b60cd7369fc1984f196f1ac4c74ff935be9cd2c4`

```dockerfile
```

-	Layers:
	-	`sha256:830e10e77c8a7bdb3112efade4c70315ac4029f3631480c163bea214071511fa`  
		Last Modified: Mon, 20 Apr 2026 17:41:46 GMT  
		Size: 8.7 MB (8667617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d84f490d5c798d85a38fb4115649300805906ef21067c0df7d162499f443b7d2`  
		Last Modified: Mon, 20 Apr 2026 17:41:45 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-18-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7fb73202b9e30a93a6c6812d3b30f7955202a8702e3b2ee477206626968db1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.9 MB (380885738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c83bcb28b52b9f5d3d932b5fdb7a7c208862b450398a5c0a91db3fac25c96b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:18:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:18:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 22 Apr 2026 03:18:43 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:18:43 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 03:18:43 GMT
ENV JAVA_VERSION=27-ea+18
# Wed, 22 Apr 2026 03:18:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 22 Apr 2026 03:18:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d07e8492bcee46202f5eae3e3010a470acc5139840e6d14556aefa3fc355f`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 64.5 MB (64479606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6c1b8b184364a826f2161a30292bce63f190c904d52be4102575e6226d12e2`  
		Last Modified: Wed, 22 Apr 2026 03:19:09 GMT  
		Size: 17.7 MB (17728884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48178854da49ba3b04c972eb9a779b3f01f7777fcf3a22c77097c13374d64a`  
		Last Modified: Wed, 22 Apr 2026 03:19:13 GMT  
		Size: 226.7 MB (226694754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-18-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c5ea3900d591b3861744a441d152abde2c2be7864a7b354de32761bd72b482ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8822520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1765021e90e0dcc1c839b0bfbf7ace92d12611aa97656bd08bb1509eb275c720`

```dockerfile
```

-	Layers:
	-	`sha256:e54443b38dddd5daeb2fe634f2d15c1b2f2e377044898355e9d6a31c7b08e374`  
		Last Modified: Wed, 22 Apr 2026 03:19:08 GMT  
		Size: 8.8 MB (8804462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27762e412b167a8a4c56edce76cb5ffd71df1a8c6b787d29fea5eb3c2ffc3322`  
		Last Modified: Wed, 22 Apr 2026 03:19:08 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
