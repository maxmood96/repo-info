## `openjdk:25-ea-bullseye`

```console
$ docker pull openjdk@sha256:af087e35080752d9450b7650bc708c6b650667c59c2e20ff08efce20e8d3463e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:926ce6032daa02fd56db631422eb6b49e9e01566584dbfab3a3783e44c5e98f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 MB (350688391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e73ee8498c113fc7468419c5380f81aa8074a9fb256131a1c299aec735fa37`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 05 Apr 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Apr 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+17
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='00bbc15cf87c83f1fe8dbd30f9ed76caff477401595491d90401b62faf63d82f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='e9a99879baf7d21abe587540977d4c09f8b79ece7a79aacdb9bf8da6c8ce9ff3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7819131060d3c79e48555fb5b04fa584b86d2fb80e3ede0864c7e6bba7d87`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 15.8 MB (15763510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f843b455b9b7bececb5cfeb4ba5839d4aa47845ded1258734c375304df3d0`  
		Last Modified: Tue, 08 Apr 2025 02:13:52 GMT  
		Size: 54.8 MB (54755152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447b6b1a7847dd9ad207fe0e1cb90b84730b4f4ff043ed7de44452748c6b8c65`  
		Last Modified: Tue, 08 Apr 2025 03:16:37 GMT  
		Size: 14.1 MB (14071460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be10a6a5494809317aa2d48ef31f16e39278a340a39b96722867a62a883f009`  
		Last Modified: Tue, 08 Apr 2025 03:16:41 GMT  
		Size: 212.3 MB (212349740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:af18206bc5a2eadac32401096ec83bc63ad5c64ec8c6378edf99c769ca2a844e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8384753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56a258dd43affd9f7b8cb9ae9517a23c0c09a47aabd227ac417d162558fe6ad`

```dockerfile
```

-	Layers:
	-	`sha256:29b5373bef4c14cc55273960074ec4b36af9452a6ab57d78d6f697729b2da55c`  
		Last Modified: Tue, 08 Apr 2025 03:16:37 GMT  
		Size: 8.4 MB (8366136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48a8d33a18e6b84554a12859eef19297756f58ce8387b7060ec5cc3ef173b4dd`  
		Last Modified: Tue, 08 Apr 2025 03:16:37 GMT  
		Size: 18.6 KB (18617 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5f980120a6ee1fdeaa15e782d918d351cac9494183cd1ca1501bbf6ad919d965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.6 MB (348559558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0ad6e6c9d7df488e0c72b0e3ab3ca402d0b26be5c01393725e096ed33a77f1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 05 Apr 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Apr 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+17
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='00bbc15cf87c83f1fe8dbd30f9ed76caff477401595491d90401b62faf63d82f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='e9a99879baf7d21abe587540977d4c09f8b79ece7a79aacdb9bf8da6c8ce9ff3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebaef8f9f6ff21c71a0e336a0e9a00fbb65d469480593ef8d1ef507941e6f6d`  
		Last Modified: Tue, 08 Apr 2025 12:18:43 GMT  
		Size: 54.9 MB (54850009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b94c975b4101ff8194268478ad4f1f062206351fdce72c77065bb99f45fb204`  
		Last Modified: Tue, 08 Apr 2025 16:30:52 GMT  
		Size: 15.5 MB (15526687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2556b7145c951d19206d6b3c348526df6b05d2ff36c85ed4efd8ad532c49a822`  
		Last Modified: Tue, 08 Apr 2025 16:30:57 GMT  
		Size: 210.2 MB (210179554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:b1eb69a1ea01f726e3c8424be23af9f2a2678f264806a9caa72e0674b3fd4e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8485859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2461b8a896702d8a768b54c8f59cd2af831a71a72dc9b7311a9f79bcd89761d4`

```dockerfile
```

-	Layers:
	-	`sha256:05bc6d1baccf638625d420f6c91ae1a10aa3a9235ea63596eaae9711643b4f98`  
		Last Modified: Tue, 08 Apr 2025 16:30:52 GMT  
		Size: 8.5 MB (8467098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5452ee5aeea3bf07eaf35240bab09ead62094681c4e1d7e80f83976c11dd0115`  
		Last Modified: Tue, 08 Apr 2025 16:30:52 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
