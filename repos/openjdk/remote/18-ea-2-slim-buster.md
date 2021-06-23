## `openjdk:18-ea-2-slim-buster`

```console
$ docker pull openjdk@sha256:f8d3c2b6d0203eef2d290c02d5187886436d61beef2c74043057bf4098572bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-2-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:44f1d211d5b1ec3502c729ce7666e93791d053204cc7a4e37f705920e87c5975
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218810224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccce48c63ce7a87b34e4f5afc40ed517c9758dd4b96bf5924d85c07363c5b7b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 08:00:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 08:00:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 23 Jun 2021 08:00:10 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 08:00:10 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 08:00:11 GMT
ENV JAVA_VERSION=18-ea+2
# Wed, 23 Jun 2021 08:00:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/2/GPL/openjdk-18-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='fa0458ce79f954b9271e5ff39815f02b8ccdda67e57791c644b331b59fe3e529'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/2/GPL/openjdk-18-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='b37a55b5a56bc7edee8b4870576338c53fc930259c630cda44fcd4fed8dc74b5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 23 Jun 2021 08:00:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee45ae9730633057cf9bd12924f9a1bf2b590631d3d085b14c96f4466557794`  
		Last Modified: Wed, 23 Jun 2021 08:12:04 GMT  
		Size: 3.3 MB (3268886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db234e0880be4c7e37162f8763ff6b4eb956e1359662d860f52f22d610690a3`  
		Last Modified: Wed, 23 Jun 2021 08:12:20 GMT  
		Size: 188.4 MB (188395487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6192efeb435721cadd3d34f8e1b3e2c9a5f8efc9112ebf929b350bff200a7a3b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216236303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4772b3863cc6336a9a0801ac344df3f3c70c5d1dbece31994156d9a545361b36`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 22 Jun 2021 23:49:40 GMT
ADD file:beee00b59da720f68e12e2ba2a8134207c80c777ddb4ceb03c71e3e4c3f51c93 in / 
# Tue, 22 Jun 2021 23:49:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 04:56:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 04:56:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 23 Jun 2021 04:56:08 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 04:56:08 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 04:56:09 GMT
ENV JAVA_VERSION=18-ea+2
# Wed, 23 Jun 2021 04:56:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/2/GPL/openjdk-18-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='fa0458ce79f954b9271e5ff39815f02b8ccdda67e57791c644b331b59fe3e529'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/2/GPL/openjdk-18-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='b37a55b5a56bc7edee8b4870576338c53fc930259c630cda44fcd4fed8dc74b5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 23 Jun 2021 04:56:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:448f6bf000e31217a7c202c659b03b7f8ac8d3ae6b03ef7a2f8339be2f00ff4a`  
		Last Modified: Tue, 22 Jun 2021 23:55:25 GMT  
		Size: 25.9 MB (25914993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb5c013aa648ff2c30dafc35db9efb2faa7f9fa6f1c98a2f31c1b5fee0334dc`  
		Last Modified: Wed, 23 Jun 2021 05:11:10 GMT  
		Size: 3.1 MB (3118894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4161f2d8aecbc20674be50119bfc8ebe68fa6c7ff40f49cafaddcfffe59aab81`  
		Last Modified: Wed, 23 Jun 2021 05:11:27 GMT  
		Size: 187.2 MB (187202416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
