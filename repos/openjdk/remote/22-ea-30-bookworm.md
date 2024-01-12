## `openjdk:22-ea-30-bookworm`

```console
$ docker pull openjdk@sha256:5a297b4c791c700eabb17b0ae7d778a21beda4a5a2be7f392d81488cb6d76d55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-30-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d440e92fb4f75d3d39ca7a5b68e021159038630c13e352460097308090af4944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357556476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58d95b59981b278c64ac65551b66397a10bffe293492880359e28bc6729ffd3`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 06 Jan 2024 01:48:12 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Sat, 06 Jan 2024 01:48:12 GMT
CMD ["bash"]
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 06 Jan 2024 01:48:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Sat, 06 Jan 2024 01:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_VERSION=22-ea+30
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='b0bc58519b965bba6505b882e5666c273ca5d2c192c44ecd5daba5efd3716ae9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e4c06460b2bf71e6f50fe574073f25d071bbde07323e02521fe6bcd7b9a4517'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d55d1cb1ffb0c7e0438b372a96cc0f23a76c21571fa3e7b7b38e3fbc66a8c3a`  
		Last Modified: Thu, 11 Jan 2024 04:44:54 GMT  
		Size: 64.1 MB (64139713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a461ca07791c619d570a2fcf6450b70c85d1edcf1c313d11035eba79bbe943d`  
		Last Modified: Fri, 12 Jan 2024 00:22:35 GMT  
		Size: 16.9 MB (16945685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf344a554c34ab20aeb06f8a145c798cb5c53e1928e6ae4c821bfab3654a243`  
		Last Modified: Fri, 12 Jan 2024 00:22:40 GMT  
		Size: 202.9 MB (202863094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-30-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d4c90f97a6120f4997710be963e29c3dd2eaf2a614136221a1dbeae198d73245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1719c2597906ff714f75462aac5f9f2edd425491e5d8a36090c9ef42e2fdfe5`

```dockerfile
```

-	Layers:
	-	`sha256:9d058e3db22c265a29c12fe3e95eacc31d609059843c95d0395d09604b2f6d62`  
		Last Modified: Fri, 12 Jan 2024 00:22:35 GMT  
		Size: 7.1 MB (7116360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16c04fac82fc99e443037d6ee43284641d04a2062136da31e4a78205fbed41a8`  
		Last Modified: Fri, 12 Jan 2024 00:22:35 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-30-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:33e0f1c61c8e34ff20ad517cc40ae49005ea635c7478803b4a419b1b7e4e7b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.8 MB (355811211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a240a481061ee9f5bb6ecce43e3f5bc1ccddc0f4710b5bac8ed0b45410f3ee6a`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 06 Jan 2024 01:48:12 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Sat, 06 Jan 2024 01:48:12 GMT
CMD ["bash"]
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 06 Jan 2024 01:48:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Sat, 06 Jan 2024 01:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:48:12 GMT
ENV JAVA_VERSION=22-ea+30
# Sat, 06 Jan 2024 01:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='b0bc58519b965bba6505b882e5666c273ca5d2c192c44ecd5daba5efd3716ae9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/30/GPL/openjdk-22-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e4c06460b2bf71e6f50fe574073f25d071bbde07323e02521fe6bcd7b9a4517'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069a35492a4c5b1727f36b1184c413a96ce816d65578adaf3bce2023a1765c0a`  
		Last Modified: Thu, 11 Jan 2024 09:34:23 GMT  
		Size: 64.0 MB (63990799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428630060163e40cf9f829265e1288a72aa00079dea1b8f66ab032378555b816`  
		Last Modified: Fri, 12 Jan 2024 09:20:46 GMT  
		Size: 17.7 MB (17728761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f894feb6f37c6356c74edf9f924a14b292c1a98f7ee2005b97b6fefebb0834`  
		Last Modified: Fri, 12 Jan 2024 09:24:56 GMT  
		Size: 200.9 MB (200916812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-30-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0efde1bf1915658a3af82c85bd733ca71500c0ff0e872e93da06f3c95cad2b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7253611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe15354d9bee063d88083e43b0fd35659473d8da6d17e0ffa103902cf689702`

```dockerfile
```

-	Layers:
	-	`sha256:b00a993d710b4b5001baf94916e5d05ff21f05ae7c1305d736fdfbb1b4b47890`  
		Last Modified: Fri, 12 Jan 2024 09:24:51 GMT  
		Size: 7.2 MB (7235187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:219a89d35fa98e14d4b4a9d6926d556a85c630daad66528a01fdbf3253d6149c`  
		Last Modified: Fri, 12 Jan 2024 09:24:50 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
