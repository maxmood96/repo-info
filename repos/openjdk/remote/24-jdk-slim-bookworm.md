## `openjdk:24-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:1b1a81544331df346ff542f73d8c2f7f8f0728660bcdfb3187889e316306963d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:0dbf9f2ef4a2864932a9a293c2f0bae828cacaf6041b1f037d7cd0d1d967e357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255412524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901878f04329c04ac8282ef0ed8f6e9358311ea5451d228c0ab32428fd97cf7e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207b2c31f2341f1243b678ab9331ddc8825e3aa6c1e421f71a4c616951ad9248`  
		Last Modified: Fri, 15 Nov 2024 23:05:51 GMT  
		Size: 4.0 MB (4018413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c553e71b98e2772a9465481f21431e92835417f63d6e11bef0bdc91d6d5ee06`  
		Last Modified: Fri, 15 Nov 2024 23:05:54 GMT  
		Size: 222.3 MB (222266116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f5d9a2cb49b5b241bddd2886092684bf7ad5417aa0584374c4ec1b994cd5ed65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acbca0efa4de036030bdcb3291d23a68b5b15f939675a8bf1554f963d240a4d`

```dockerfile
```

-	Layers:
	-	`sha256:1bdf7fb68f3458df6d8e17cc9580517cc7853b17f4b083d4785a406e21357a9f`  
		Last Modified: Fri, 15 Nov 2024 23:05:51 GMT  
		Size: 2.5 MB (2534207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84acafa63d8d3e77858df6e3e0037b85febe7ddb3926f09f622b26c461b0b687`  
		Last Modified: Fri, 15 Nov 2024 23:05:50 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b703d70728f81c20f669a5abe0a37a37b262c7dd74c4ce4bf8bce42234bb79ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253208026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cbb2a9938757e5f4deace5d84326c00aff744ab890dc0e0b931f309b7c594ae`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc98f864523d3ac886c7499edaf8b2161f61a569e2f1a6d4e5a8dbfbe62110e1`  
		Last Modified: Tue, 12 Nov 2024 18:44:24 GMT  
		Size: 3.8 MB (3833706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724bf86bec73c491c96b396b99ef608d07163f4949494cb075376a774cb2a601`  
		Last Modified: Fri, 15 Nov 2024 23:12:00 GMT  
		Size: 220.2 MB (220216964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ce70a4b9c7b6a13e97b21f11c7fc7bd8b7714f3f7963ac7152e0bfed43d8ceb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3036438e353fc8ee1af5b5f1b64106136ae66c5954fb3def8d40627158e8bd2d`

```dockerfile
```

-	Layers:
	-	`sha256:560fb0f55133834d7a7100d591a0ca624451775f0ede73d1fd0dd55537c6de82`  
		Last Modified: Fri, 15 Nov 2024 23:11:55 GMT  
		Size: 2.5 MB (2533935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:440d311737497d21722de0cda24e97184199dfdaaff66c1c5f8f045c06a7a51d`  
		Last Modified: Fri, 15 Nov 2024 23:11:54 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
