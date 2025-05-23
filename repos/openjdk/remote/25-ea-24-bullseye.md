## `openjdk:25-ea-24-bullseye`

```console
$ docker pull openjdk@sha256:6d5c1b671a8b20cbff1b702e93fc119d58980c5ca1a9379bdbcf354925af5bda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-24-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:58fdd6bcec21fde7325160d1d4bc742b8697fc78c7adfac9b36fbfe7cae66514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.3 MB (352321985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9a8bfea5a0f886c3e4fed2f82bf153d9031aba8a7dbdd20c7dc25aa11ae226`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 23 May 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='e47e49dfbb2ad32aa825a587f7aa6829a8ba6fac2b7f60d4cf5f38d8c5241c3e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a4306d6d5c87e8c33dc9a7cffa13b9c984f7173cc4921bce549781c5ada23cd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 May 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Wed, 21 May 2025 23:20:29 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69a02035012d2783a66ac7ecc549af09c1718d81affa5f9c39abcf969da971`  
		Last Modified: Wed, 21 May 2025 23:37:39 GMT  
		Size: 54.8 MB (54757308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a0f2494fb2356e2be69b764ca8306c1e65d88ac1b1b161c463dd7a75d21a5e`  
		Last Modified: Fri, 23 May 2025 19:55:15 GMT  
		Size: 14.1 MB (14073086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ba9ae0d719a57ec8fb15c719ca96fdb8dbcf7f927ae58657a7e2609579cbf8`  
		Last Modified: Fri, 23 May 2025 19:55:21 GMT  
		Size: 214.0 MB (213976522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-24-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:767c69cc386ad39bba719250f9abec2d54a96b5e32a6f8f255b9d35111ee13e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8420929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d263cd5b5470d5d1d2de5082d37d1c72d858fa1bef55558d1455915a35daf032`

```dockerfile
```

-	Layers:
	-	`sha256:f9449f6e7c9ca5e9815ccb03c514df801632bbb0d32152dc3862a007ff04b367`  
		Last Modified: Fri, 23 May 2025 19:55:15 GMT  
		Size: 8.4 MB (8402311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd6dd92dac6616d08693f55394eb7a952f4d6dd3a27a51af1a147363a58fc4e`  
		Last Modified: Fri, 23 May 2025 19:55:15 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-24-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:88786c8d88be817dcd07eaa708913baca1cc0561d5eec82a6f5e75fe0835b88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350132556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169b05286935f58057a3d8e6c4658dabba35332a47e10a125ba7b505f4ad9c81`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 23 May 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='e47e49dfbb2ad32aa825a587f7aa6829a8ba6fac2b7f60d4cf5f38d8c5241c3e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a4306d6d5c87e8c33dc9a7cffa13b9c984f7173cc4921bce549781c5ada23cd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 May 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a602f78cf8d696db9521d18affb7ecdb79ff690533efae26e3bdb1544cb1752`  
		Last Modified: Thu, 22 May 2025 02:47:52 GMT  
		Size: 15.8 MB (15750382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1b27af19f7550ac0d9c38bf6bcf26ba7eb53984e7e5e0886342816133c76e`  
		Last Modified: Thu, 22 May 2025 09:18:36 GMT  
		Size: 54.9 MB (54853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9676be39ecf6cb9e3f4e79710da294a95dac4f569aff09dd3c46d0c48ba0126`  
		Last Modified: Thu, 22 May 2025 13:04:06 GMT  
		Size: 15.5 MB (15527614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d697506ae11bccad286f88109898374509a4f95635a7ac4fcc40561a00e868c5`  
		Last Modified: Fri, 23 May 2025 20:08:13 GMT  
		Size: 211.8 MB (211753569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-24-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:4c44bc646d96d2a7d7f3da00d861c00ad134b9c2bc0dd026a1da962dfafd31d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8522034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33a1b8e799877fc5293367d1acfeb73e8eba2566b348bed5a8a0bc34970cb26`

```dockerfile
```

-	Layers:
	-	`sha256:81d8f3bfd3c8e56f82618300aadf10ee45fc98032bb7040edfd82038ce5d616b`  
		Last Modified: Fri, 23 May 2025 20:08:09 GMT  
		Size: 8.5 MB (8503273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1ac07189659342e6485ea30ec55a17d6cd4325815eebc54c60aec8b633598b`  
		Last Modified: Fri, 23 May 2025 20:08:08 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
