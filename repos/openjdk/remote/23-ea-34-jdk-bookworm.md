## `openjdk:23-ea-34-jdk-bookworm`

```console
$ docker pull openjdk@sha256:5e98fb7275c8bec19d0e6e0a63e6b31f8e669be4ba056fc50f819c7bafd33053
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-34-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d1420705d641f8021e973b1574e338d89b0d7c943f9a154d72521a33245a90bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366121256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da106fe56feaa4219ef5a09e9f62af7cb4fcba11acb0d3b5ac9bb0932fbc049`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:03 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Tue, 23 Jul 2024 05:24:03 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jul 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+34
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='9d3fa4fbb8247f3a47788c52c09ac5c265e023cfda821610ade2a43104bdaace'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='f79a40a5860e7b57ced61d19167847390dbe4f370c7511cf7923f75d4a546363'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d643a5fa823cd013a108b2076f4d2edf1b2a921f863b533e83ea5ed8d09bd4`  
		Last Modified: Tue, 23 Jul 2024 06:13:33 GMT  
		Size: 64.1 MB (64143199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a821a2421f7567e7a1dc6e9f2565dd81c0b11504579803b9afdb936a211f3e`  
		Last Modified: Mon, 29 Jul 2024 16:56:39 GMT  
		Size: 16.9 MB (16942991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3234ed2f3d6daae82eb6796c47c047f08c59ce0266d03f2b9eaf4311a257e924`  
		Last Modified: Mon, 29 Jul 2024 16:56:42 GMT  
		Size: 211.4 MB (211430195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-34-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:44165f2c8811d06d2b1acdba34a6e9fe747b83e17969798720bd9190fec8c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8276457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab984d212bcf6fb8980593b87bdef21159aad656de8b4851969243d4c5aaaf5`

```dockerfile
```

-	Layers:
	-	`sha256:215486449b03d9b129dd33781093aa96b67fe660b04aa147f6289433023352a9`  
		Last Modified: Mon, 29 Jul 2024 16:56:39 GMT  
		Size: 8.3 MB (8257994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc4a1fd0e2255ae6c62dbdcc3264bbae5c04f8af0beaddc93cf4fdee3f8d264d`  
		Last Modified: Mon, 29 Jul 2024 16:56:38 GMT  
		Size: 18.5 KB (18463 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-34-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:715d2bd998e2d8e6eb4b9814c12474e068a215cfca6c62b5d9fb8c86c5ca9a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364201913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd87f720eb9ce5635334c8ff6be38d1da91fbc91f268cae7b2033eb1cd91c41`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jul 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jul 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jul 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+34
# Fri, 26 Jul 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='9d3fa4fbb8247f3a47788c52c09ac5c265e023cfda821610ade2a43104bdaace'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/34/GPL/openjdk-23-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='f79a40a5860e7b57ced61d19167847390dbe4f370c7511cf7923f75d4a546363'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jul 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e903e4e709d192e5547602a5978c79692063228a98585f33fb02d343bc15719`  
		Last Modified: Tue, 23 Jul 2024 08:10:20 GMT  
		Size: 64.0 MB (63994288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad2e5609f4bf13e28a549241365ce86413b647e67b95cba7c36a2233342908a`  
		Last Modified: Mon, 29 Jul 2024 16:59:05 GMT  
		Size: 17.7 MB (17727179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ec1a17b177fbc421272e4d0d5b324caa17bd7bff9cca4bcf5d049a57674c7c`  
		Last Modified: Mon, 29 Jul 2024 17:04:37 GMT  
		Size: 209.3 MB (209299551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-34-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:841470fe43228ceb6f86a92b3019c08b2e809dfb5dab5e05a1296b619915a778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8414458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb10d05781744e8e4657a7ce2b87762b5f9165d735c2446a35051bfe17dfefc`

```dockerfile
```

-	Layers:
	-	`sha256:87959e0fa6e79b76a0d34a7caa2d1a78714394fa62387251792b6c8ed6b4456b`  
		Last Modified: Mon, 29 Jul 2024 17:04:32 GMT  
		Size: 8.4 MB (8395655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7bf9df4a42dceab9eeca084ee692960e173d9a126301ba6596f0b9898f736d7`  
		Last Modified: Mon, 29 Jul 2024 17:04:31 GMT  
		Size: 18.8 KB (18803 bytes)  
		MIME: application/vnd.in-toto+json
