## `openjdk:28-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:cfccbbda2e9c3e54fe3843099032bae2a01a07fb102f296d0c8eeffc8caf46cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:c4e31a3d462ec38119cd00043e7bb364cdfdff6942d960aa96e9e33f94354da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259457366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9b8475899e5ee420db2cc0ba0e3d235fd465d93dc842dbf7e77a68122b6136`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Wed, 10 Jun 2026 20:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jun 2026 20:16:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Wed, 10 Jun 2026 20:16:53 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:16:53 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:53 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:16:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 10 Jun 2026 20:16:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89ec250d63998fc9c7d3ed45ff2a146a6cc1f6db47426b145cc7aa115acf9b3`  
		Last Modified: Wed, 10 Jun 2026 20:17:14 GMT  
		Size: 4.0 MB (4032994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7c1f13afb8c83e238bb714f337b743d351080ea15233a25c474941e195caad`  
		Last Modified: Wed, 10 Jun 2026 20:17:20 GMT  
		Size: 227.2 MB (227190829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a09f1395961ea57ec5e7bccd44b35cbd0b4bef5b72a737bd72cfe0c5266f7368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2664118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f6e75c5e99faac34b30258c1dcc9aeaade4850ac7fb01d7a80d1ff16721813`

```dockerfile
```

-	Layers:
	-	`sha256:8070bfe4c15818a24267429ba71e967ec5c4c1358cd1d213e892f833ad2ea4d2`  
		Last Modified: Wed, 10 Jun 2026 20:17:14 GMT  
		Size: 2.6 MB (2647260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:848c3b6ce77ea1fed6f4bed28e95ed121f7c631adadc67d7361db6005effa887`  
		Last Modified: Wed, 10 Jun 2026 20:17:14 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d0b56cb10f061ec948c25debe911c214c91c8edec38fe702d607c96dbfe3cefd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257126996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038eb6d163e126ad5da52bdb783b61a845725d595de2b2fa2d7ec559951b61db`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 10 Jun 2026 20:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jun 2026 20:16:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Wed, 10 Jun 2026 20:16:37 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:16:37 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:37 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:16:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 10 Jun 2026 20:16:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610b2f98a5ecaffb28f458a72f1f7b021ffdb3dbf40e31c8891b04007f26da16`  
		Last Modified: Wed, 10 Jun 2026 20:16:58 GMT  
		Size: 3.9 MB (3852860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db0b48144aafd6116a246c8e0130d6c34c59a14e1a9d0b9bf3f9ae4fab30cb0`  
		Last Modified: Wed, 10 Jun 2026 20:17:04 GMT  
		Size: 225.2 MB (225159093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:9ef9af28fbca37aaa15abcea344b1ec8968d5b663487373ecb3b32e00d18e12e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2663871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1d8c06c241c9d348fc8f9d7cc351a47d0e784e7426e8467082cb6c04c9273a`

```dockerfile
```

-	Layers:
	-	`sha256:ebb1770ee0d58b679b4a618e70e0c82500e25a84ce283d0fdb0c8026c3c06647`  
		Last Modified: Wed, 10 Jun 2026 20:16:58 GMT  
		Size: 2.6 MB (2646894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96759e364c8ef91ca33ac0a649221b00c4fb0748f82ec613aff75bbf9a3ea821`  
		Last Modified: Wed, 10 Jun 2026 20:16:58 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
