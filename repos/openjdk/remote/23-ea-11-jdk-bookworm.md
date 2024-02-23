## `openjdk:23-ea-11-jdk-bookworm`

```console
$ docker pull openjdk@sha256:5d22985311757d2be673ea9fd1a4fa2f73ac334bb7d6e0e53a2a26a0f7bfd992
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-11-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:498af8b4a7ef0b2490a9e87d51513920a4bce41afdd6abcb3983624b53735183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 MB (357902883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599cc8f764ffb5bb618f6eefbe3f848745550fa7422bb41e53e23f9ee833d6db`
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
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 23 Feb 2024 07:48:15 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 07:48:15 GMT
ENV LANG=C.UTF-8
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_VERSION=23-ea+11
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='e297d7f6d296a96d9b3c30a8ab90ab911fb920560690f4b77168b6b6fbde162c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5d67060b45e0752b89e71a8d98a36978ac8528efbc12eaded427ea8c0f69b90'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
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
	-	`sha256:b8ea9bd103012817e83144632d06484cbb9a7287dbda43a9a9e56787b930ea79`  
		Last Modified: Fri, 23 Feb 2024 18:51:25 GMT  
		Size: 16.9 MB (16945792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c6d7dd05dd669b94a34b5bb48869912f7a9d08c590b10877d2ddbe2890340b`  
		Last Modified: Fri, 23 Feb 2024 18:51:29 GMT  
		Size: 203.2 MB (203217581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-11-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:7968a4f6176be2d98fc29407171b61193631f06751a8c85425a200196d0c0696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8248108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879330cf4cb21d46b37e06225bf65d6832d9dd458cdd2e932f1171dea4caae27`

```dockerfile
```

-	Layers:
	-	`sha256:56b50d1544949275c8dd085897da5f780efce3bba2a6d6b2f2204f6080a9a93c`  
		Last Modified: Fri, 23 Feb 2024 18:51:24 GMT  
		Size: 8.2 MB (8229201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f1229493aa8a8ca181c7d60c368f4c3888711720860856323a03e8e7bdef43`  
		Last Modified: Fri, 23 Feb 2024 18:51:24 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-11-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:15a7d3d5da543c1d1b58a8cd47cf8a2d1129aaf9f86be533f240d9b42391cd14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (356015330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d2da73faa868a15b6eaef92db1a2f0fc1e0aebfbb01d28c0ec2780054e8e11`
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
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 23 Feb 2024 07:48:15 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 07:48:15 GMT
ENV LANG=C.UTF-8
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_VERSION=23-ea+11
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='e297d7f6d296a96d9b3c30a8ab90ab911fb920560690f4b77168b6b6fbde162c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5d67060b45e0752b89e71a8d98a36978ac8528efbc12eaded427ea8c0f69b90'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
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
	-	`sha256:702d088fe65d83aa17a804646db340a06b5e83c87ecbddb4eb129f3311311cff`  
		Last Modified: Fri, 23 Feb 2024 19:03:52 GMT  
		Size: 201.1 MB (201121786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-11-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c4b43859450ae36181c960e85e112133c82f943e147a9ea59671060a3df514b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8384262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb506355915a7a51f0ba6c34248d88598c8aab931ab82510ef20983e404900c`

```dockerfile
```

-	Layers:
	-	`sha256:f6abe00e54c836d910e20a77b1063dee525e7df69573d08fbfa67905e7dd413f`  
		Last Modified: Fri, 23 Feb 2024 19:03:47 GMT  
		Size: 8.4 MB (8365838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70f789164cc3340e627fc6b1e6bb58bce8389a8e3b4d513234673436c9d4c64f`  
		Last Modified: Fri, 23 Feb 2024 19:03:46 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
