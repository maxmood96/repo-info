## `openjdk:27-ea-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:0c850c664c1683f59f441d1e37f9fd8090d21d628e9ca37553a25859d56062d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:e2c43db52431703e31ae1ef9a92057ac12cddc22704efdfeb7890b888d7deaf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260700579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41486402ab89cd7bbd1d6f3ad0bfb1ce15a0838ebd908035072728e60da102d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:28:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 24 Feb 2026 19:28:22 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:28:22 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:28:22 GMT
ENV JAVA_VERSION=27-ea+10
# Tue, 24 Feb 2026 19:28:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 24 Feb 2026 19:28:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccf7de4dae1af2fe55cd9097c1466d8df3dcb29632472f6ec553d4815a50347`  
		Last Modified: Tue, 24 Feb 2026 19:28:42 GMT  
		Size: 2.4 MB (2370987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f429001df9bffe76c92190e0ed863821f6c88d48513e8b0556e8ee86c187e3af`  
		Last Modified: Tue, 24 Feb 2026 19:28:46 GMT  
		Size: 228.6 MB (228550960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:a5a6488e9e3021c1ca8c778075537c6e7b19fb987c26e3e9784308d5050c4dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375ce839dbf45c3bdc2972e596adbb6cca8203b0ffc6ba4262b71d3743f84052`

```dockerfile
```

-	Layers:
	-	`sha256:9350492f54f159d63f38c2dc25cdece588aea43c6869ab4eeaa402f00d0ff010`  
		Last Modified: Tue, 24 Feb 2026 19:28:41 GMT  
		Size: 2.3 MB (2278857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e8925df23c1f8eb7305e6c2ce19adea180f5c982d57be26da196aee505c08d7`  
		Last Modified: Tue, 24 Feb 2026 19:28:41 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:91bbe92d951c4bc1a5b0b4f3eeadce1ed614138933f5cb4b1c9d0e74c73a8e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258958360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a2311613b7401b2eb88ad336741e964033905d4f96192a596fb694cce894f2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:32:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:32:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 24 Feb 2026 19:32:59 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:32:59 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:32:59 GMT
ENV JAVA_VERSION=27-ea+10
# Tue, 24 Feb 2026 19:32:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='d42a6202d27fdca3cc1de29d07dc85bb73d27637ba1e1ed715357472da050d31'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='91f6dae354fee821c0052fdbe9acd9f894976596733268741b65d4a4a25ec686'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 24 Feb 2026 19:32:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8125a1192fa4396b2548de4df5c38f6f1f674ffb8124c7b65f11692f19b2b705`  
		Last Modified: Tue, 24 Feb 2026 19:33:20 GMT  
		Size: 2.3 MB (2314397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254ecef16ae0ec248e1cd0ed3b67025441bb23ef793a417a1ae929cdfdb66fd2`  
		Last Modified: Tue, 24 Feb 2026 19:33:25 GMT  
		Size: 226.5 MB (226503865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:ea7dcc2e0dccd3b341fef782f66780e5756d9b68ad33881d4d789c562978744c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8001a13f10d20cca788ea9f90bf96e70e0ce07c45b7dec1da4e89fa73c22b2`

```dockerfile
```

-	Layers:
	-	`sha256:658e225744dbe865923d0b5eeb33f386367671c53c4a543eed63395bb0dff8d9`  
		Last Modified: Tue, 24 Feb 2026 19:33:20 GMT  
		Size: 2.3 MB (2278543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5feb59b9e32df158b1bd1ea937155d2fa2b3c578e1a5a3759d3c11d7816283c6`  
		Last Modified: Tue, 24 Feb 2026 19:33:20 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
