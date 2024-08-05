## `openjdk:24-ea-9-jdk-bookworm`

```console
$ docker pull openjdk@sha256:287df4ff7fa7e5361508c09253fecd37c92e763abed82e3d46de4b8013664c5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-9-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:7683a2e626c602b42750745ab01f8fdfce462ca7dffacc585fb31b67134b28be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.5 MB (366529458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4c8a7f45bdf88abee46570c3cbd169af1b009d7208834cd4d370c4b63f519d`
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
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 02 Aug 2024 18:51:57 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:51:57 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_VERSION=24-ea+9
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='5dd8d67a4e4059d22eb6fe7c636bf7610832380061f522aec631b69fdbaba6ae'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef04b828af0fa6aca544841b01f5efda63143b81f52f1f69b2b5cf46953713a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
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
	-	`sha256:d435053207ab90dbfb762fdc5aed2b6b40d9ac094d189b13d4b60a463078cc21`  
		Last Modified: Mon, 05 Aug 2024 18:58:28 GMT  
		Size: 16.9 MB (16943054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e65aa023ad51b353fa610f391d24ddf285055184551b9813aa25394f44df26d`  
		Last Modified: Mon, 05 Aug 2024 18:58:30 GMT  
		Size: 211.8 MB (211838334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-9-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c1cb148f436a4fca7b343464e05b4af0d9b8fe46ebd3109fba8c0837128f7c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8276431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91493b4f0b8ae9ec3abac3e4fbd1124c7b0fc712cf9dfd45f10782b43247eafa`

```dockerfile
```

-	Layers:
	-	`sha256:ecc911e56ffa863003c9b18e61fad4c01e0df5c3a002047b92218ccb5f17afcc`  
		Last Modified: Mon, 05 Aug 2024 18:58:28 GMT  
		Size: 8.3 MB (8257986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11b0f5fbd5cc3d1a90a29897408e44321cb546d269511852975c77984c40078e`  
		Last Modified: Mon, 05 Aug 2024 18:58:27 GMT  
		Size: 18.4 KB (18445 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-9-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4f6f3d53f63db32f74ce6d4062f08b635ecb9f645092aad63c9967cecd6fd25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364618016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86258a9fe2441c400e1657930667966120774cf9480580e606fc7ac9221010eb`
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
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 02 Aug 2024 18:51:57 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:51:57 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_VERSION=24-ea+9
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='5dd8d67a4e4059d22eb6fe7c636bf7610832380061f522aec631b69fdbaba6ae'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef04b828af0fa6aca544841b01f5efda63143b81f52f1f69b2b5cf46953713a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
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
	-	`sha256:90fa5e37b3e36d057966efd023d08de55a02a719d3ce74ffd5db4297278fd133`  
		Last Modified: Mon, 05 Aug 2024 19:08:21 GMT  
		Size: 209.7 MB (209715654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-9-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a1c548751365d4479fc834937342fbf32752559eab971b9edc84d091a6d2c585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8414433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa6220156e22047b48f9edf53fdf90b629252b6262dae2c0273ab5055877aaf`

```dockerfile
```

-	Layers:
	-	`sha256:5d81e66c134ebfaabaeb443d1675ed69c64716676d232d6cd09a97b36d150ef8`  
		Last Modified: Mon, 05 Aug 2024 19:08:17 GMT  
		Size: 8.4 MB (8395647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7924f51e6bca0be57441d7770643f4066845954c4ba41cfea1f2c47b5987ad19`  
		Last Modified: Mon, 05 Aug 2024 19:08:16 GMT  
		Size: 18.8 KB (18786 bytes)  
		MIME: application/vnd.in-toto+json
