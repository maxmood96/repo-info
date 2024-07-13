## `openjdk:23-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:bdc1c9eb5b3a4f59ffe80f583544d1f5ef99454b914fb5ea697b565164a3fb43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:b0007e37d642c2d47effcdfcfe5c9864033776fb3ef18c074363075efd60893c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366109093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed79ba9d5c3f880dd517271e501798ab64655bc10cf40bce7c131d7abe31b4e9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 01:24:49 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 02 Jul 2024 01:24:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:48:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:48:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Jul 2024 06:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='49af9ea82c1a9396a8c8529334d26ec7c835b217c790965708fbdbf29fb46ba2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='2bde94ea8c9261ad53a1644b2e04cb13a6ab4c95d2649beff2cbd6f176b8465d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbed71fc5444cf6889a21b002de3e7805e810aa88f91a9ca941b4e3880246d1`  
		Last Modified: Tue, 02 Jul 2024 02:00:35 GMT  
		Size: 64.1 MB (64142928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d38b34e8457d4a8f159db20dcd6871cc46e565c87ebb4d288cdd3cd5a4deda0`  
		Last Modified: Fri, 12 Jul 2024 21:57:24 GMT  
		Size: 16.9 MB (16943056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c5000011162184ccaec8fb7a59ad7355ca8f3f2902d4319d7f4b45b93a21e2`  
		Last Modified: Fri, 12 Jul 2024 21:57:27 GMT  
		Size: 211.4 MB (211419251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2d50b5c0be7c609698a6352a1552b7596f27410c5c023662676ae7d1721c4587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8239621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a2b42178034817aab36ab036d5fe146febb5a9137b642b20b60e95f768a7c0`

```dockerfile
```

-	Layers:
	-	`sha256:0f4c711df1fdf486236d60275160b1d2c47ea5cc100b06b4fffd18ba8bef4f80`  
		Last Modified: Fri, 12 Jul 2024 21:57:24 GMT  
		Size: 8.2 MB (8221158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:115eef4609f99c43279bfec54d43e43dba0d7c1a0d5c379addd4630d84ccf2c7`  
		Last Modified: Fri, 12 Jul 2024 21:57:24 GMT  
		Size: 18.5 KB (18463 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6e9e4f1ab9afe81b2000ab72bff4959f13950b0a10dad659b122109d89649d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364212442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60dc6f71fb664ebedbf4ebb7a4f1a704d29e99b50a534e071ad802372dbc1c7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:29 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 02 Jul 2024 00:39:29 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:51:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 12 Jul 2024 06:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:48:10 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 06:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='49af9ea82c1a9396a8c8529334d26ec7c835b217c790965708fbdbf29fb46ba2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='2bde94ea8c9261ad53a1644b2e04cb13a6ab4c95d2649beff2cbd6f176b8465d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6ab51b82df5ee608db374a16686eefb99bc53834af17064184653121729b3`  
		Last Modified: Tue, 02 Jul 2024 04:01:58 GMT  
		Size: 64.0 MB (63994637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde725b95df667f4c7a75f1cbb9ba4e44a03c657cc943acba90627447298e297`  
		Last Modified: Fri, 12 Jul 2024 22:06:49 GMT  
		Size: 17.7 MB (17727101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29138885ec43b17c9925051db842378771428658540fc42b333ec60be68af7ed`  
		Last Modified: Fri, 12 Jul 2024 22:12:14 GMT  
		Size: 209.3 MB (209311111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:16cbcb71bc9b27a4ca32b30212dd7a82b671877ca71bc6dfabb0cc9ffd18f030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ad6e08109757a30c227bce98fecf4a503ab0d88d3b77c6df31aec3d84bc933`

```dockerfile
```

-	Layers:
	-	`sha256:4f6f1ab59301e9130d335184c042881e56c8933b9f449a731fb699ada047fd73`  
		Last Modified: Fri, 12 Jul 2024 22:12:09 GMT  
		Size: 8.4 MB (8358819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80324b15455d373a864a3729c09872200cff2fc1d32944b940cd40225d23585c`  
		Last Modified: Fri, 12 Jul 2024 22:12:09 GMT  
		Size: 18.8 KB (18803 bytes)  
		MIME: application/vnd.in-toto+json
