## `openjdk:23-slim-bullseye`

```console
$ docker pull openjdk@sha256:dc5c3ab67575b973246f839b8b12598e5a96f74e5faafac045ed412c319560b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:6dae9561ffc26c2bfdec061f74fa485283b9aa46b19a45fff722754d149c167e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244003291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edb6c47ca987607f1630a8fb60be8658f6d682752daea985f0d55ea8c97e4d1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 29 Mar 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+16
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='9a5d2039ec965c15d80dbc5106c9e2f1c4a80975e18d308b55f0a3d892f24358'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d654c940f0c5b9ed7549f29066599b2caedbaf2ec45f3745ac35e265c288e2d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a740543af2fcf184cd25960920287bee1cbe96e0eb70a2c0e40b8b45139bac69`  
		Last Modified: Mon, 01 Apr 2024 23:49:57 GMT  
		Size: 1.6 MB (1581793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632b1058adcf08ec32ba8e5ab27aaf3bae480c4ae2ab1773b1f58900314f9420`  
		Last Modified: Mon, 01 Apr 2024 23:49:59 GMT  
		Size: 211.0 MB (210999009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:87715568b1244700009abccf68fcbe874ec62cb469e0259594847721363f78ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2517285e09899f2c778701de0bbdeeffd5137ef1d881faac043baec8cd96b8`

```dockerfile
```

-	Layers:
	-	`sha256:d23abf216b462be368cf302996a1a4b6f43ca6af0bdf0748fe3b1aa6e0dcfd7b`  
		Last Modified: Mon, 01 Apr 2024 23:49:56 GMT  
		Size: 2.6 MB (2638334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44906573a5878876c2415bb91735d090dc1c4fe29dec6f2b13782ea143edff39`  
		Last Modified: Mon, 01 Apr 2024 23:49:56 GMT  
		Size: 17.5 KB (17472 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6f1a2da26976593dcbc784d3dbf9fcf04380831956b74da07f2f6fd605fee426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232409120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8553050dbccab4eddc5bcd8e074798560426f4d9b8e16410ece689ac52183f2b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 22 Mar 2024 18:48:16 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Mar 2024 18:48:16 GMT
ENV LANG=C.UTF-8
# Fri, 22 Mar 2024 18:48:16 GMT
ENV JAVA_VERSION=23-ea+15
# Fri, 22 Mar 2024 18:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='c17995b5c67b845af47704e2a664f5b6ab540f968cfae06972a7562144b7634a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='804a15db8c406a0d70ad5a2da125339de3ff66759107fdd75bc6323d6d0cc5d4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Mar 2024 18:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a999e7ea0713e0f70812c73c3a44d4933028059c0e0e95008ffb99319b0d52`  
		Last Modified: Sat, 16 Mar 2024 15:56:11 GMT  
		Size: 1.6 MB (1565943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772a569dad6868ed531268b5a43d116a73703b4c9c4641e53192265bb44d103b`  
		Last Modified: Mon, 25 Mar 2024 19:59:28 GMT  
		Size: 200.8 MB (200772061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3a517297f59c23d0613b64bd1092a07d4a60d0ede196457b05228c4fed8d2b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2654905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3fbc5116a097b5ee28cac14764f62cc636478226246e4d89a832eff6480a9f`

```dockerfile
```

-	Layers:
	-	`sha256:b9c45a17f70b2bdd0b0d273237f65ac467bd0165e62ab100a35f35e238f091f2`  
		Last Modified: Mon, 25 Mar 2024 19:59:24 GMT  
		Size: 2.6 MB (2637586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7aefefbae95e6eb246f8f502a6764d33bf3887e78f5e73d6df5caa13426ba6`  
		Last Modified: Mon, 25 Mar 2024 19:59:24 GMT  
		Size: 17.3 KB (17319 bytes)  
		MIME: application/vnd.in-toto+json
