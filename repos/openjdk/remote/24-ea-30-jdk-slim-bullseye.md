## `openjdk:24-ea-30-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:0121767358b086a017ef5be25db9f5b47bb6a439f288a05fdc6f8c4048c69b9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-30-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:3a0e4fbd89ec2783be34e8fc940c7243e29ddcf0735de20a08edd0a3871b2355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244556705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e685e4ed1c1a49556a1acf98dc77db2684f8f793e591fcbab761a3b86ac2d842`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 03 Jan 2025 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+30
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='613ff61d4553e9e8c17793cec42c93db99b73ee18bb41d5ceefcdcdfee0d826b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f89ccf3b004d95bdedd0fdd10cee362f00be006ebe79a394b0539057e8d8ff6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34a69bce82e17063da3413dae70d9c837750dbda225063a65fbc3446f05ae68`  
		Size: 1.4 MB (1377215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af3b064edc1d9ca90eacd2194d42aa6071025cdaed443600cc658427ce9075e`  
		Last Modified: Mon, 06 Jan 2025 20:28:05 GMT  
		Size: 212.9 MB (212926847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-30-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:c0c87e595f648be03ff7a7680cd790dcf5f74ddc7c74a62a989bd3d16b6cb4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcfaf2b67263a3dcb52ff7110dae5cb7d3352593c377f50ef95dd6beaf6c9614`

```dockerfile
```

-	Layers:
	-	`sha256:9c36f235c409cc3a60bfd0493aebb683969b8cc24c2552deb07a39228e67da57`  
		Last Modified: Mon, 06 Jan 2025 20:28:02 GMT  
		Size: 2.8 MB (2827922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:350ef209abbc4e0e79a06f839db75af798b6f47c9552849e0683d4d8490a141a`  
		Last Modified: Mon, 06 Jan 2025 20:28:02 GMT  
		Size: 17.6 KB (17569 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-30-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2deca5dc86b7627fd21fc32df32e16cd2c1a757abd5b383d9b4389c6b3e4cf82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240977162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5a657cb7df4589c85946d966acaecf5b156f187c493ba4a51416d982c2928d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 03 Jan 2025 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+30
# Fri, 03 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='613ff61d4553e9e8c17793cec42c93db99b73ee18bb41d5ceefcdcdfee0d826b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/30/GPL/openjdk-24-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f89ccf3b004d95bdedd0fdd10cee362f00be006ebe79a394b0539057e8d8ff6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802af25e15e1605893bc7f616bdceb6df54d42569f2584718a22b15a94ff45a7`  
		Last Modified: Wed, 25 Dec 2024 02:34:25 GMT  
		Size: 1.4 MB (1361263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92c0dd7afae65b55c51baa1219645f86beb289983bec610ab96fa5b630f739a`  
		Last Modified: Mon, 06 Jan 2025 20:38:10 GMT  
		Size: 210.9 MB (210871046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-30-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:2b9d248a21c7577e34a2b8a39555b9114020659cd8dda2eae6d5c514a41594fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2845287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce71fe2c8299d2d8a587844d84c15b73032f5a9667c7e314e2733f5cbcc5effb`

```dockerfile
```

-	Layers:
	-	`sha256:2a23c66348f6ec28ebc3ff539103dd3d36a2ecd5a16b38ed4f6870c2d170ab90`  
		Last Modified: Mon, 06 Jan 2025 20:38:05 GMT  
		Size: 2.8 MB (2827574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33dcd869362bd8342b912a52f87a3bd2b74c715f72cecb63dd8d6d803cf827c5`  
		Last Modified: Mon, 06 Jan 2025 20:38:04 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
