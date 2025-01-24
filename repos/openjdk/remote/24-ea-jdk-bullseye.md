## `openjdk:24-ea-jdk-bullseye`

```console
$ docker pull openjdk@sha256:4c1e8ec7661d70599368ea6881859401aae92a8032b34c5fd5f1378f6d0a70fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:32f0c98f4fee05800eb5b5a98fafd8b6efc09edfe2aa693e9072dc711b272b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (351009405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bbb12495bb4860653608b966b791dea3a28bd6c4fbcdd3943a9a15441447b0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 23 Jan 2025 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='52afbfd5229250d1a724367cda6380f2acff08c58ee9bfcc6db727ccf4feb251'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='4c6890d8da82bc38820c3b8330579c9083a6dbc834c5026def54e9b83bc18dbe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
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
	-	`sha256:7ccd8698d5825711d0629cbc7ad6be99c549add2dc3405526973f311067ddf16`  
		Last Modified: Thu, 23 Jan 2025 22:26:43 GMT  
		Size: 14.1 MB (14071492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e443e5ce00a604f24fce310fbdd7ce005aa9ed0e8e3c355cb941946cd45120`  
		Last Modified: Thu, 23 Jan 2025 22:26:50 GMT  
		Size: 212.9 MB (212886853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:5fce8354db08dffd37ebbe567fa913b3d64e1fc4b001d565e65d0ae3c840e809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8383403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e20884404db6888894d8cceca54cb666fe15b1d4796180cdb353b5e7ab398c1`

```dockerfile
```

-	Layers:
	-	`sha256:ee689da70c222a3bd010c0686f20c3d1664280c89ec49f5c2a4bb35c3802c722`  
		Last Modified: Thu, 23 Jan 2025 22:26:44 GMT  
		Size: 8.4 MB (8364785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cfad8c13aed46669787ccb29944739929caef3901e6324b33a8e178de279583`  
		Last Modified: Thu, 23 Jan 2025 22:26:43 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d17d0a84180be1cc0f0e4108b64b3843bfaad5f7ca173142ff339e70f345e056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349004602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dedc5df51d9cb6aa42caf479db7245c25923743363d1c89cf2857685de6d50d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 23 Jan 2025 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='52afbfd5229250d1a724367cda6380f2acff08c58ee9bfcc6db727ccf4feb251'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='4c6890d8da82bc38820c3b8330579c9083a6dbc834c5026def54e9b83bc18dbe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
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
	-	`sha256:4484a2f63acb29001777a3a91c0d68937768a923a4b5eb83756b3200c0d01946`  
		Last Modified: Thu, 23 Jan 2025 22:32:50 GMT  
		Size: 210.8 MB (210835537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:495b6ce6522599ba6a36064b970684359f1fcfe091607e44439116b359398010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8484507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80de0cd4a9effd11b3ec1d5713d032b8ce6da29493fb16f779c9afb48e4b5396`

```dockerfile
```

-	Layers:
	-	`sha256:bab7263d1fddd95d40581a762fa8c8a09b60416ea498b0d244938efdb599c1f1`  
		Last Modified: Thu, 23 Jan 2025 22:32:44 GMT  
		Size: 8.5 MB (8465747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4be94676d17296020a29aa5b4c282753c97e8bf3208e524737cb2b80b24ebb0f`  
		Last Modified: Thu, 23 Jan 2025 22:32:44 GMT  
		Size: 18.8 KB (18760 bytes)  
		MIME: application/vnd.in-toto+json
