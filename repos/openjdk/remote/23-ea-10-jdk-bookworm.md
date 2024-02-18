## `openjdk:23-ea-10-jdk-bookworm`

```console
$ docker pull openjdk@sha256:d54dab2c19e8090292ebdf35889fc6006f4599008cab3edf3acc40ba96d50084
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-10-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:0e909c346dd1777354057d013ef35df25d7a98edac7966b6fcf88a564d748f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 MB (357904856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b878005f87ac29c29e547348d407e5ebdf5f528af8929386b0b730eb2bcc10`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:21:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 16 Feb 2024 20:22:31 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 20:22:31 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_VERSION=23-ea+10
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='9b583a20351ff9be1b782ba71d5e61d7f8e4731c81277e4f2566c5509db052b0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='b646bcb58d932236e066c97dbc32d6df53a9a823c78565cd22bd6bf05a0cea7d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b40be4436eff6fe463f6977159dc727df37cabe65ade75c75c1caa3cb0a234`  
		Last Modified: Tue, 13 Feb 2024 01:30:58 GMT  
		Size: 64.1 MB (64140328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7593f981ab638b9d7a8b68eec72cad5469a8d813357e86e38849095af7a75443`  
		Last Modified: Sat, 17 Feb 2024 00:53:41 GMT  
		Size: 16.9 MB (16945715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4a77b1f927b6694763a3893833d803e0b4f0f750276fd0f111fd930389f754`  
		Last Modified: Sat, 17 Feb 2024 00:53:43 GMT  
		Size: 203.2 MB (203219631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-10-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a320476ef2298406239603f535bb9399863355fe3a0f0e0c81ec4ad0838ee60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8248108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60992d860d120d3489fdb6951422c500933f0ff2682e54905fc5ecdda9e5d45d`

```dockerfile
```

-	Layers:
	-	`sha256:f4b531dbf2d413ea4ee847e0dcd2eaddb336c79df3d49fce8b0c07f101fffed0`  
		Last Modified: Sat, 17 Feb 2024 00:53:40 GMT  
		Size: 8.2 MB (8229201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c577229463955cfcd64d80f05ddde8b1c383801f8d1808334df4c49b1a02b44`  
		Last Modified: Sat, 17 Feb 2024 00:53:40 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-10-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ce8306553782834f6ed7659b498375359816f8b7379605700a4693479333b2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (355990293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fa8424b4c9d2820087184027f5f2b429f5d892d6a2808856239af190ca6308`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:37:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 16 Feb 2024 20:22:31 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 20:22:31 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_VERSION=23-ea+10
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='9b583a20351ff9be1b782ba71d5e61d7f8e4731c81277e4f2566c5509db052b0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='b646bcb58d932236e066c97dbc32d6df53a9a823c78565cd22bd6bf05a0cea7d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ae72c83b17aae41ce6857f0063bfd35b5f00dc5d7e1ad47fa18debb28b2c7`  
		Last Modified: Tue, 13 Feb 2024 01:46:49 GMT  
		Size: 64.0 MB (63990920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe14a5e4476942656d1cabdd2cbdcf3021e0b986bfb394a9bc0c3b1cac79b12b`  
		Last Modified: Wed, 14 Feb 2024 01:15:20 GMT  
		Size: 17.7 MB (17728893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971876cea830a250ff0ede369ce787c1885b9ae95b7c345ed7b885de2e5b347b`  
		Last Modified: Sun, 18 Feb 2024 05:17:32 GMT  
		Size: 201.1 MB (201096749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-10-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c8e0014914d4b4e9c821320804b93e078284d5b6a82fd0faa81465ed74c5bcc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8384262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b69eb5185256dfc8b22e819344bf99ac8dac46a45ab4ce0c3f81978a68f43ba`

```dockerfile
```

-	Layers:
	-	`sha256:3a93133ddbc074db4071ccc02d7117058fa484b941776971f2c75910384df922`  
		Last Modified: Sun, 18 Feb 2024 05:17:28 GMT  
		Size: 8.4 MB (8365838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e923e07552acea89530e8bb1a18b170ded8a16b7ec5d37560513d64e1a55ce9a`  
		Last Modified: Sun, 18 Feb 2024 05:17:27 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
