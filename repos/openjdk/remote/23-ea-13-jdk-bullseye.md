## `openjdk:23-ea-13-jdk-bullseye`

```console
$ docker pull openjdk@sha256:e0914accf4de179ecf64d0a19440900e89ae85dc26a5421cbb91b53ef1987f78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-13-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:530e32659e3e9fbcc4fadb81347200bd86433170684e9b444bf383daa049bbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342430370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6327a705c296047032458301213a112d9de1ddb3d5e71eeb92d215a78cff1fe`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 01:48:16 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["bash"]
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 08 Mar 2024 01:48:16 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Mar 2024 01:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_VERSION=23-ea+13
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='f805f5ac203384c50ac3980796a4c4d92d1e21b0ead0c9870e1ed8edc9e2588b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='061adb6d88422017ef07f10561bd9b551f22e36b7db0860e1505900d8f5165f0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b4675e1918dcb7f5c9bfedbb5a8634d2459306d1f3b91f08c7293380f10585`  
		Last Modified: Tue, 12 Mar 2024 06:03:29 GMT  
		Size: 15.8 MB (15763469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f67b1746a83d257a6398cf8eec47bfa1f854670097ea4234f12857cfc7d5932`  
		Last Modified: Tue, 12 Mar 2024 06:03:46 GMT  
		Size: 54.6 MB (54588494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f372a07db64d9ae08ff39104a2fde7e940e0754a383402a3f521e260527e503`  
		Last Modified: Tue, 12 Mar 2024 06:58:11 GMT  
		Size: 14.1 MB (14071293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8b48b507944e50aa8f01ac724c9d784fb7e3b59dc3419a493c158609cc2444`  
		Last Modified: Tue, 12 Mar 2024 06:58:16 GMT  
		Size: 202.9 MB (202922145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-13-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:7ba03ca71dce68c951580bf906b8d9adc5c37f40c006af5a0f71f68f07668b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8175946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6c48182f0fbf016f2bfa0b398394d11f72445aeac6a9e038965bfd6321e8a9`

```dockerfile
```

-	Layers:
	-	`sha256:f0e4586265aabc82a80584cad8dd06e191a7f920d5c366d7750c5b84fc6930e0`  
		Last Modified: Tue, 12 Mar 2024 06:58:11 GMT  
		Size: 8.2 MB (8157039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d26c75523b25c26460203cfb77705e8ac10a1aea7f567bbeb565cb5d07a1749`  
		Last Modified: Tue, 12 Mar 2024 06:58:10 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-13-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:34e071345570f4df8fc14e7b1cb40b00bb6116ccb5e17d0d903e0c42d4b76231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340479566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3e7e4a0b649b14308d4ae48063b02cd2f8c9cc4773763dadc8225894de8b0e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 08 Mar 2024 01:48:16 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Mar 2024 01:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 08 Mar 2024 01:48:16 GMT
ENV JAVA_VERSION=23-ea+13
# Fri, 08 Mar 2024 01:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='f805f5ac203384c50ac3980796a4c4d92d1e21b0ead0c9870e1ed8edc9e2588b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/13/GPL/openjdk-23-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='061adb6d88422017ef07f10561bd9b551f22e36b7db0860e1505900d8f5165f0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 Mar 2024 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d359f54bdf6c7734649777e288d4d317d49bd63e944dd5f852641a97b61527`  
		Last Modified: Tue, 13 Feb 2024 01:47:39 GMT  
		Size: 15.7 MB (15749141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c2c85b768f52fc0353f0af0e43d671b1d1025996f39d238e750611070d206c`  
		Last Modified: Tue, 13 Feb 2024 01:47:53 GMT  
		Size: 54.7 MB (54693679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c873e2cbf63de85cd2f48b4b8921c08c57ed0d32b5c275bf7132160b425e51`  
		Last Modified: Sat, 09 Mar 2024 04:00:37 GMT  
		Size: 15.5 MB (15525886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d02c3700341ffabc16f790af00fdd51da5c78c9559fe972f65eec2db15fb62`  
		Last Modified: Sat, 09 Mar 2024 04:00:40 GMT  
		Size: 200.8 MB (200789374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-13-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:a8839109c588202a68cb857f6f19956ae96edf3a8f0e2c8ef77e950f7ddfac61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8276151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c990b460c4ce7fa59f11bf1ce5cbc5a92c3654ce47d2f424bbbf0033b20d9971`

```dockerfile
```

-	Layers:
	-	`sha256:167a2a4f19cfedc2e613c87885a5d7e498bdca41d56b56d83816218902bb44b3`  
		Last Modified: Sat, 09 Mar 2024 04:00:36 GMT  
		Size: 8.3 MB (8257727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ac00e40e2a0f2e115d300fb34cc11bd40f941e410fa7316af2e17046052c896`  
		Last Modified: Sat, 09 Mar 2024 04:00:35 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
