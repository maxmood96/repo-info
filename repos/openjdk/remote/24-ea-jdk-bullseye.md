## `openjdk:24-ea-jdk-bullseye`

```console
$ docker pull openjdk@sha256:1790c1deb26132e0ce3e36677e7f0fea6464d0d4a0911f1d9ac1a5268729d361
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:718dee7e27b3787a9afeac7b8d0ce05726f292d782771946b14c740ea272cda0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352176927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e2606343b0b9067813182bceb089744b4e4e3e887337d7a77031507f0bf153`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c539c6f53265d7398b56c208ca7cbf4f16d1714d21b9ed251a77bf75966bc2`  
		Last Modified: Sat, 19 Oct 2024 00:54:50 GMT  
		Size: 15.8 MB (15762308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07a20b182d5672c6ec8dca30220175ce5c60e45bf630d6adae50504d92368ad`  
		Last Modified: Sat, 19 Oct 2024 02:06:22 GMT  
		Size: 54.7 MB (54725293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac934cf6d47cf19df964df1faca0c3d8aa3a636a6da3e3a5531e59fda97bfc5`  
		Last Modified: Sat, 19 Oct 2024 02:54:41 GMT  
		Size: 14.1 MB (14071339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e708b1b2cad1575263895c1b7d7c3ce6a26655689015a78e6c2f0d1aa73b55`  
		Last Modified: Sat, 19 Oct 2024 02:54:44 GMT  
		Size: 212.5 MB (212537376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3510d0f7463feeafd56d6b969db65dbf041979c92dd57906d7a3b03133aab158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8374439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b23aa5d10ae60521dd0b313f79460e49061e4ebea6fdfc39ee2c47456a642ce`

```dockerfile
```

-	Layers:
	-	`sha256:9579609c4fec942f9b07e1d8e127732156d2475f2dbc10c00152a9940af8b745`  
		Last Modified: Sat, 19 Oct 2024 02:54:41 GMT  
		Size: 8.4 MB (8355822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:124ae6a38d2c60116318b7e02edeebffb4b0e79b3f59500b168922f4ce14504d`  
		Last Modified: Sat, 19 Oct 2024 02:54:41 GMT  
		Size: 18.6 KB (18617 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5edd31888a2db3454647511cfdf407460216f1a75f3a7e75d4d20151c76c9452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350088327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4cef2fb6be5e5ea9201ef08181cfff42dcfaec865de9dfe4d56fae6ba8fefba`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 00:48:11 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
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
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181aac8447b7f0be083cdefe7039dafbc9a5e8c0a2c94de7b46d053e538a50d8`  
		Last Modified: Thu, 17 Oct 2024 04:37:01 GMT  
		Size: 15.8 MB (15750225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0134077e35514883cdc89f46185c7eae106a74a0895bfbc1494fdde44310f977`  
		Last Modified: Thu, 17 Oct 2024 04:37:14 GMT  
		Size: 54.8 MB (54834752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6638fd20138002a59aa27da4fcd76f4a1c3fffa258b931545a9de63ecf9054d3`  
		Last Modified: Thu, 17 Oct 2024 22:04:47 GMT  
		Size: 15.5 MB (15526098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdef145ceaae4505e6a134135448818527d2199debdbb03c10627bf74c593892`  
		Last Modified: Thu, 17 Oct 2024 22:04:51 GMT  
		Size: 210.2 MB (210242357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:600b1a455d98b249c659241d85b8c17225c819486fdca5ed690572f65bf84692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8451720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da58af52f675e6668fb79be4c7b4c11be2d53e419710a707f160bf77b9b6139`

```dockerfile
```

-	Layers:
	-	`sha256:326f99f2746ef55cae4be719159c0b1f7c9163e947a3255e0cf18e80dafd4652`  
		Last Modified: Thu, 17 Oct 2024 22:04:47 GMT  
		Size: 8.4 MB (8433082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05df2fb85f2113dc20ac6c13d684d2325d6bc046d46432b7ce988a148d29241d`  
		Last Modified: Thu, 17 Oct 2024 22:04:46 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json
