## `openjdk:24-ea-23-slim-bullseye`

```console
$ docker pull openjdk@sha256:4fd055a7a1d4bee151a8c8327273cc1f1821ee02845bb596e141c75dc1297763
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-23-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:7c135cbced4f7f0a4c5f10747ea395b6fc2a369ee6e56f44b4d5ad4246b1d053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246360223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a80f81fb9d86b4eddd9ef3dd30e3a2fd9f096d01168dfaf7ea5a1b7d69c1849`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Nov 2024 19:48:11 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 07 Nov 2024 19:48:11 GMT
CMD ["bash"]
# Thu, 07 Nov 2024 19:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 19:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 07 Nov 2024 19:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 19:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 07 Nov 2024 19:48:11 GMT
ENV JAVA_VERSION=24-ea+23
# Thu, 07 Nov 2024 19:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='4a83df6c5ba87f963cb8f7830f1ddef7dbe387b6884749411cdd4db6f3be6ee4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='76fba0034d8bd3edd8983162ebe459dfcdeb8d19e0202eb42803716fedf61a32'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 07 Nov 2024 19:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4c61d1bdafda5117543d142b627a93d494aee1bdf8a2cf3508005675915031`  
		Last Modified: Tue, 12 Nov 2024 02:44:19 GMT  
		Size: 1.4 MB (1377307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dab9d35aaa3d90e3a57333883d3cbd792392c2e52e6915661ec94a0d76862ee`  
		Last Modified: Tue, 12 Nov 2024 02:44:21 GMT  
		Size: 213.5 MB (213531355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-23-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:5ad0a001646b91c6b61951e68d03f37056df4a7547988a0afa020c40cae39028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2828373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca48530088edd2ffe7c6ad11ecfdbf9a53ddedb2d5856994ab4388ee7e827cf`

```dockerfile
```

-	Layers:
	-	`sha256:ea5448539ebc9048dec12a962fa64a41e8467988b5ada5ccf3e6deab244f226a`  
		Last Modified: Tue, 12 Nov 2024 02:44:19 GMT  
		Size: 2.8 MB (2810804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f570e1a4c5b5eac93d367bcccf592b0f623d0ffb4560b2435069513ff2d0941`  
		Last Modified: Tue, 12 Nov 2024 02:44:19 GMT  
		Size: 17.6 KB (17569 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-23-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d06728ba44795696c31da703b81dbc4b420d933bb1d2d70cd0f386cadb6026a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243110491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7829aa5e259f3c23bf2f80ef66561948ad5b11c65acecc1c70ac71ef4ed75034`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 07 Nov 2024 19:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Nov 2024 19:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Thu, 07 Nov 2024 19:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 19:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 07 Nov 2024 19:48:11 GMT
ENV JAVA_VERSION=24-ea+23
# Thu, 07 Nov 2024 19:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='4a83df6c5ba87f963cb8f7830f1ddef7dbe387b6884749411cdd4db6f3be6ee4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='76fba0034d8bd3edd8983162ebe459dfcdeb8d19e0202eb42803716fedf61a32'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 07 Nov 2024 19:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee6a91206e970280650395d7f0f6464fddada0d19449f16f2b817c35d488480`  
		Last Modified: Tue, 05 Nov 2024 00:16:09 GMT  
		Size: 1.6 MB (1565956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7236d8c84a5e19ee20711fb248adb0d69d381f8b3df11411304f0ac3a78a46b1`  
		Last Modified: Sat, 09 Nov 2024 05:12:36 GMT  
		Size: 211.5 MB (211468778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-23-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:c015366277b2dea879da03bcc56be37d4381625c00c8fb15dc44bf6948d2f0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb85e0081491d13ef69dee5a60a972c5241dd95c0da5f06cb65dae9b3f39410`

```dockerfile
```

-	Layers:
	-	`sha256:d593638d413cd02db37893417c9c620c664e53314cd9cfc9e0f6c73852e4d790`  
		Last Modified: Sat, 09 Nov 2024 05:12:32 GMT  
		Size: 2.8 MB (2812004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7017901961e2848b565c05449bbf669ce4d93587e8488db982a209beeee948f8`  
		Last Modified: Sat, 09 Nov 2024 05:12:32 GMT  
		Size: 17.5 KB (17528 bytes)  
		MIME: application/vnd.in-toto+json
