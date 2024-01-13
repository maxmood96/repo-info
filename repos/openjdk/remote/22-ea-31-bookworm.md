## `openjdk:22-ea-31-bookworm`

```console
$ docker pull openjdk@sha256:1a45fadeea5052974bd2facc55051d84aab52a93686093c1e88d2814673ecea7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-31-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:26a577aa2f1e63eac00b2f9dd1411e8d130bc3ec90caee7bbb937a09bf814fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357568749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370a024819e0bff62ce11046dc30edfa93552071e527fe727be894cd7301a16d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:35:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
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
	-	`sha256:4c3b018d7545b338baeac3e0f4288d566cc8d96b0d9f5bb6074cb0bffc8d9661`  
		Last Modified: Sat, 13 Jan 2024 01:07:36 GMT  
		Size: 16.9 MB (16945690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca10ecf090720c6ec474c02036c2fd3d714d2c45b28b5ca9008341dc4ce331e`  
		Last Modified: Sat, 13 Jan 2024 01:07:41 GMT  
		Size: 202.9 MB (202875362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-31-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e0bd725d830a60ee2280beb1706d10702d681abc8e70e7ef1312984246164d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012ab492ce46000e806b3f625c67011c62f0d4bd3f18120fd1fc8d9d7092e723`

```dockerfile
```

-	Layers:
	-	`sha256:6047602d800b47e733e6512a713f9c29d87cf2c72a63eb9dd01b2b3f4ceefdff`  
		Last Modified: Sat, 13 Jan 2024 01:07:35 GMT  
		Size: 7.1 MB (7116360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c7ce3ec39dfb3e54c5d476ab89cdad1ac1f81d394985cc5083173ae7260989e`  
		Last Modified: Sat, 13 Jan 2024 01:07:35 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-31-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:100238856026ea1b0461f7fa2a85315f689bec820b58b482d794e36e041d7763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.8 MB (355830346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79255f0213bfca734e930d16780641096cfc56b2c861c8e311e66a97a68d0011`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:25:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
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
	-	`sha256:870932f917a3157a6ec2ea13b958443b2cab519bb516271fc6570019512f5ffa`  
		Last Modified: Sat, 13 Jan 2024 01:45:10 GMT  
		Size: 200.9 MB (200935947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-31-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:6df6e0784084151f3576a40058b25b7640b3de349817d175017560fbccb8a049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7253611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c114a2c6cf55acdd8407e18abf55eee262da9d51abc624192d8b2505c98dcf4a`

```dockerfile
```

-	Layers:
	-	`sha256:ac7d411db8a410b9dc62800dc492acd54d9d64d5c85aab16c9c6a0b351e5fff6`  
		Last Modified: Sat, 13 Jan 2024 01:45:05 GMT  
		Size: 7.2 MB (7235187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c8ce5ade917239d4d658a017491b8d3cc2dff0cdfc5380710e580f2903c818`  
		Last Modified: Sat, 13 Jan 2024 01:45:05 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
