## `openjdk:25-ea-7-bullseye`

```console
$ docker pull openjdk@sha256:a1efd2be4b0a3bdd41fd4f8dc1deac754cc162a37b4caa656678d1dd43a74ad7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-7-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:3153d8a0a81edf845e9f7e9ba9f3bda7f407c064d7a9c6369927a31b54cb8291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.9 MB (349921276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5bab41eba2b749f3d49ade69675f2c4abbd991f699b2ddcd1deaa81451fa49`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 25 Jan 2025 01:52:19 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:52:19 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_VERSION=25-ea+7
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='7feccd12886711c8902b12a7af32cb26a34993f148b00a36aa93068ce1e3b128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='8f29e5e012a3477812ef892a16022af8410235782f12c41d09d2a7082e20849e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df16681c019573e3211da3a69493c28abc41e22e0cfaaf006fa4e8a20965295`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 15.6 MB (15558362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d363a1dd2d1714709c84ac8d050f51e921efc51885c202b336cc24f61e3186`  
		Last Modified: Tue, 14 Jan 2025 03:18:11 GMT  
		Size: 54.8 MB (54753534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0431cc315a0a2db6784ce7230b495ce819b14733a8e6439209c325a0969ebdc1`  
		Last Modified: Tue, 28 Jan 2025 23:28:16 GMT  
		Size: 14.1 MB (14071489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4018073857c3833cd6d4571943114b5d3906d25b51b76115e89bbadaabd6d3`  
		Last Modified: Tue, 28 Jan 2025 23:28:19 GMT  
		Size: 211.8 MB (211798727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-7-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:7b07482ff4dfa57e841556b917d1fa652a513c844aaa2d6b9d6a46a90b538d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8382748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd570494147c687ffe9838e39f0b7f52fff317d8598e3f0c04fcb42c7f5aeec`

```dockerfile
```

-	Layers:
	-	`sha256:9723c3ec0b3daf586544384943546290f1895fac996a196dc7b69696ea10779e`  
		Last Modified: Tue, 28 Jan 2025 23:28:16 GMT  
		Size: 8.4 MB (8364148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f58bc0bfcf7bd81ad6f3c93b8d56159cc7be4074cd96e36785d40236dba1b6b`  
		Last Modified: Tue, 28 Jan 2025 23:28:16 GMT  
		Size: 18.6 KB (18600 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-7-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8a7a4b2b1b9db1437b59f36b0229ff263696a2ed36ddcd1cac5c83d06a97c878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347929964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8365ca0c1addf0d6a85d9b794b99bba5c0ee2e49f4f41e9ba138f3a31774d929`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 25 Jan 2025 01:52:19 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:52:19 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_VERSION=25-ea+7
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='7feccd12886711c8902b12a7af32cb26a34993f148b00a36aa93068ce1e3b128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='8f29e5e012a3477812ef892a16022af8410235782f12c41d09d2a7082e20849e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d131bb45427773e6afabd46e2adb4b244b25d4dabe87133f23082bb3234e33e0`  
		Last Modified: Wed, 22 Jan 2025 02:33:12 GMT  
		Size: 15.5 MB (15526310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972376b1ac5144773f8549c62d66ec931b729eb9778996aaf2d485a6c107dbcd`  
		Last Modified: Tue, 28 Jan 2025 23:35:56 GMT  
		Size: 209.8 MB (209760899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-7-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:8aa7e843e23a7be8666fa0c5f1c7460e1707ccf97140c7b39190bca143e12812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8483854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d769e12eda42195b795db289036df5f75c72d4881cfa2a05e51f7112bdbb75`

```dockerfile
```

-	Layers:
	-	`sha256:cbb1a9f30aeef8e635bb454498bdae27f94eeb73661052a0430ffaaf976697fa`  
		Last Modified: Tue, 28 Jan 2025 23:35:51 GMT  
		Size: 8.5 MB (8465110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8432aebb947d1e576e14f2d2071e559c8141199dd76cbeeb0d0a4ab397930a77`  
		Last Modified: Tue, 28 Jan 2025 23:35:50 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.in-toto+json
