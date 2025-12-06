## `openjdk:27-ea-1-bookworm`

```console
$ docker pull openjdk@sha256:b7be15df38bcefb0592aa5d7bbc512d82a830ad8ad7d06526b829cc831f0ff82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-1-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:460a61a5436069dacccf7065a52168646e42a16fdc61dcece0a7f1c594e4ea60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381853794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4275dec6679db4ec3fc761f8a39db07f1a4e466c32b9886e6418acad29f87560`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:34:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 06 Dec 2025 00:34:58 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:34:58 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:34:58 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 00:34:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:34:58 GMT
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
	-	`sha256:baebed1ed2d11b15a486b1c8d2acb3dfee3957416552703a7f1ca0e166f75c4b`  
		Last Modified: Sat, 06 Dec 2025 00:35:40 GMT  
		Size: 16.9 MB (16943714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1cf2ea02a6aff1fdceb1768941646ae9cde6a20561ee80acb16f60cb328f44`  
		Last Modified: Sat, 06 Dec 2025 00:35:49 GMT  
		Size: 228.0 MB (228003709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-1-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:867855f0f931d4bf93e5bd2b4f66c18ad3c166239e77094755b092cf11350716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9bbc4dfe57015c6c17afa227c9cb990ba822ff71356ba59b5da260a2610825`

```dockerfile
```

-	Layers:
	-	`sha256:d955edb203db0b6d608c00ed629a557d97f55433321d81a472796e4064cfdbcc`  
		Last Modified: Sat, 06 Dec 2025 01:26:14 GMT  
		Size: 8.7 MB (8668188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2466d1fe43bdebe0ed7a8bcdb508532d19354528cc90117a36f2eabab6611f31`  
		Last Modified: Sat, 06 Dec 2025 01:26:15 GMT  
		Size: 17.9 KB (17922 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-1-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:80a0b4175b5fbf736282e37338694d4d39de24c4a478ce9991454ba699aef839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.0 MB (379966870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92be5450e71301174fb473129b4c8dd5c4ab9b73da4a6611af1e608d57e00087`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:34:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 00:34:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 06 Dec 2025 00:34:18 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 00:34:18 GMT
ENV LANG=C.UTF-8
# Sat, 06 Dec 2025 00:34:18 GMT
ENV JAVA_VERSION=27-ea+1
# Sat, 06 Dec 2025 00:34:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Dec 2025 00:34:18 GMT
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
	-	`sha256:a57f2563c09503d30fc39f18df1278447dd4626debd72fda460a445822880ed8`  
		Last Modified: Sat, 06 Dec 2025 00:35:03 GMT  
		Size: 17.7 MB (17727757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903e30a9208f7a0cb1a2ba9d86784db678ee4c520083c87c7db76da39421173f`  
		Last Modified: Sat, 06 Dec 2025 00:35:13 GMT  
		Size: 225.9 MB (225910241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-1-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3b61cb7c8f03b4cdf8fd58943c50446a52f9ea55a6a8a70d0c7defa37b5cb8f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc11e6e82cc2a40a35b6ee2c921e2b56453f3b6475942d8263a99294a5801293`

```dockerfile
```

-	Layers:
	-	`sha256:26185e8822995a3f7c172d382be44e4fbda56ff57083c4d2eb226e1d7aa37544`  
		Last Modified: Sat, 06 Dec 2025 01:26:23 GMT  
		Size: 8.8 MB (8805033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73199990562cc85036e9bc5f5dc363134445467b67f75c372fb85c38e37cf72f`  
		Last Modified: Sat, 06 Dec 2025 01:26:24 GMT  
		Size: 18.0 KB (18040 bytes)  
		MIME: application/vnd.in-toto+json
