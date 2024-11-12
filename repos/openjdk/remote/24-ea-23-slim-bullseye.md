## `openjdk:24-ea-23-slim-bullseye`

```console
$ docker pull openjdk@sha256:b76af3b248acbcd94ffae671900e9fa8e2f869688598e5733a5fb6e983e51928
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
$ docker pull openjdk@sha256:39fdef098a743fd0ab35c25873916cd30d3f5f1603bb531f0de10baac51b5278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242921667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecaf8b106cd61bd9a377fad804607f69d402d057026cb3cd49b1cebd5c9ab020`
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f8956420fad8a33c8d0ab8fce67143e196e496b54a2ab0a2d2bc4d9a2ad45`  
		Last Modified: Tue, 12 Nov 2024 18:45:19 GMT  
		Size: 1.4 MB (1361337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e070624b0a6e433ba92ec811ac99b77c609ee731d4ba5cd666536829462f04a8`  
		Last Modified: Tue, 12 Nov 2024 18:45:25 GMT  
		Size: 211.5 MB (211468730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-23-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:0b58f2a8be22353bb5c1e97b064a2d2ecd62f12b1c6d1685e9c72bca1ef4f011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2828167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7146acb962718d2a82ff4ea087a17c13a15d58adbb8135df9e4d076fa721c1d7`

```dockerfile
```

-	Layers:
	-	`sha256:40412f8aafbb225560dcdd51704c75b36665193e6ee17dce36d8eaf4078969d7`  
		Last Modified: Tue, 12 Nov 2024 18:45:19 GMT  
		Size: 2.8 MB (2810454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64a8e706cfbf29bb9648f3829064a890a30a28228c0bd0b367e30029a210d480`  
		Last Modified: Tue, 12 Nov 2024 18:45:19 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
