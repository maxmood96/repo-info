## `openjdk:22-jdk-bookworm`

```console
$ docker pull openjdk@sha256:b103e7052b04d3121d71161c2ae1f4c1dcf1ddb925bb36fe4fb230aaed485f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-jdk-bookworm` - linux; amd64

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

### `openjdk:22-jdk-bookworm` - unknown; unknown

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

### `openjdk:22-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:50dfa6195ca5dd5328c02f7aaedf2e107c0e5af8660a0f75dd67cacf00f76a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.8 MB (355808280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d48b29ad36e1c75a2020a501c3f1ebf19fee2d0265c2068740f3acecdd07f1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:34:00 GMT
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
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c641d36985b2db859fc64c43a6dbf7c25cdf73e5d16d107fab1d95a840bb4e1`  
		Last Modified: Tue, 19 Dec 2023 11:42:17 GMT  
		Size: 23.6 MB (23582271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd8544b6e15c7a4096b1f48a67fb5bed2efba509fca597f1c164b582ab01c02`  
		Last Modified: Tue, 19 Dec 2023 11:42:35 GMT  
		Size: 64.0 MB (63988289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f4486e748ebca87a82800520024d71377305cb16a0c8e2cfdd5de9220f3e9b`  
		Last Modified: Wed, 20 Dec 2023 10:21:15 GMT  
		Size: 17.7 MB (17728700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410dc2a2bb9fdf10ee93d4ed8dec4377cd169b743a3d7d50d801717f47fbb993`  
		Last Modified: Tue, 09 Jan 2024 02:25:45 GMT  
		Size: 200.9 MB (200916761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2e82fd392025bbcdafc8529d211c3e4336d6732fe9e693afc31caccefa094f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7253610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3532e345cb3be5114d2e21b608491efa66766374667ba1b67cb71f6f4131bc7`

```dockerfile
```

-	Layers:
	-	`sha256:03335ebc74dac535d4284fd48fe5a4f850b84e58e1ccf94f7aa56b53ad0cde6c`  
		Last Modified: Tue, 09 Jan 2024 02:25:41 GMT  
		Size: 7.2 MB (7235187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d7ba00d43e81105f7b08c4d9148c95b4b35eb2410ed785675c8544c721ffadb`  
		Last Modified: Tue, 09 Jan 2024 02:25:40 GMT  
		Size: 18.4 KB (18423 bytes)  
		MIME: application/vnd.in-toto+json
