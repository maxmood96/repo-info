## `openjdk:28-ea-1-slim-trixie`

```console
$ docker pull openjdk@sha256:bfd9ed793d64815576b214858bbd0d19ebdda7fbf0a7b71b369c06332cce1672
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-1-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:911d2e26bbabc7066a2ea279b7148132f39bc9d180a9307af59b639367812189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262307691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07c948f33511a769b127042bf9594fa1a010520c0e7294235efbdca8660d274`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 10 Jun 2026 20:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jun 2026 20:16:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Wed, 10 Jun 2026 20:16:43 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:16:43 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:43 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:16:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 10 Jun 2026 20:16:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4f9df963d3b31e1813fdb701b1d69b6a3f7ae4dc48c2e868d5acf1338f1073`  
		Last Modified: Wed, 10 Jun 2026 20:17:01 GMT  
		Size: 5.3 MB (5335171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e970f67cb467d6278b01078d396e27384d92547a9aaed4857afd9af0c34fc3`  
		Last Modified: Wed, 10 Jun 2026 20:17:05 GMT  
		Size: 227.2 MB (227192594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-1-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:ea87a2dd97fd85f66713d3ba384e6b49f4503176ad36c5d4ee727e4df165b551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab1749c63a82a965056ca39401a050d782c26ffedd162a7636aa31b6ec5adfd`

```dockerfile
```

-	Layers:
	-	`sha256:f0e97077dedb961a7df2cf5ad1c07b0bab8b4df70cf1a2ca6da1f9dbed1a8e62`  
		Last Modified: Wed, 10 Jun 2026 20:17:01 GMT  
		Size: 2.3 MB (2276368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d88dd0f6600e68cb8eeff439cbaf16e9a891c273ece73df22d44a9c4280770c`  
		Last Modified: Wed, 10 Jun 2026 20:17:01 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-1-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a2a2fc40de00c4d1ba659a8c8c888f2749dcf976f579f9ee50fa85dc8e145748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260949440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359e6fc6f36bb4cfbd45dca34a19c5b172f4d59dd58401b2854a41b788b3ced4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 10 Jun 2026 20:16:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jun 2026 20:16:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Wed, 10 Jun 2026 20:16:29 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:16:29 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:29 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:16:29 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 10 Jun 2026 20:16:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c184b234b5eec07de9159c7d6abb3f413c481527babb3df99223eccdeab0ed53`  
		Last Modified: Wed, 10 Jun 2026 20:16:50 GMT  
		Size: 5.6 MB (5646688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e90edf98e9fb68516748278448def26d20b356426abf3b78ddc283cfd67b1d`  
		Last Modified: Wed, 10 Jun 2026 20:16:54 GMT  
		Size: 225.2 MB (225160833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-1-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:becbbc5d955c53eb9dfb73973730dd8e7dd1cc741a3a6cbf842ef08adf5f6ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629993f8041bd3dc358598b1144a745d32e5d72ea3344478939ac127fbeb86b7`

```dockerfile
```

-	Layers:
	-	`sha256:b098bf6e02c34e831e0c5b748b5a596da63e147a52a507b0ab12e75cb717e83a`  
		Last Modified: Wed, 10 Jun 2026 20:16:50 GMT  
		Size: 2.3 MB (2276046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8315f22500dcd670c3c4325cb6a716174d51983e918e3994cc0fd1f508db1aaf`  
		Last Modified: Wed, 10 Jun 2026 20:16:49 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
