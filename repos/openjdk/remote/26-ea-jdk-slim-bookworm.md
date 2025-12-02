## `openjdk:26-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:353ba54fee47a635e7f0522915205088e473ef2ab100612734e2473ac571f281
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d122db8e93cf3a0fdd85264745ba72036976c3578ba914b6adbc75d643fd317a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260032635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafd2634083f110e8a084aacb69618586c999e8cb36d656a080bfe69f9e58379`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 02 Dec 2025 01:08:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 01:08:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 02 Dec 2025 01:08:36 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 01:08:36 GMT
ENV LANG=C.UTF-8
# Tue, 02 Dec 2025 01:08:36 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 01:08:36 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='b44fa2d67d24735bbcd2378df77b3afd2c5313bd275072e7d328718e2ce3fb11'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='dd0c4a9fc8008b0aeacadecd8df3373b395ed4d4d3fac501218d512ca509d178'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Dec 2025 01:08:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a7f097b21a60aaad2a1e0bf3471b9f4d6bc4b09a6a87272c3ba0dcb98da4ea`  
		Last Modified: Tue, 02 Dec 2025 01:09:23 GMT  
		Size: 4.0 MB (4027371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b950c2c9b09d89eab44631f58e9b2eaec7c9a07d32e5c150d181027ebe888c0`  
		Last Modified: Tue, 02 Dec 2025 01:09:01 GMT  
		Size: 227.8 MB (227776815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4901036e5b5293586ae9a1ba72775aecc0e555762377a63f41015450f34240ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1f762f0ca81796f39cfeb941022a69f8ee5fc0afb80fde7fdf67d9b956f12d`

```dockerfile
```

-	Layers:
	-	`sha256:5e904e59d2b10e076ecd608f93ddbdf32a13af78708186168cdc1c6e838ef399`  
		Last Modified: Tue, 02 Dec 2025 04:24:15 GMT  
		Size: 2.6 MB (2649789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a0a5326c472f6ce23c57f6fcbe30ea05015c1cfd5c6d3ad0fe48fb84c32e147`  
		Last Modified: Tue, 02 Dec 2025 04:24:16 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1369ff1f095fce415947eb5482af7aa2a42ed536389244792e1841ca288abda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257654781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feed7a697e427b1b934bc7821d341236c46f0d4ca8d60613b8cc703fc5db621`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 02 Dec 2025 02:33:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 02:34:04 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 02 Dec 2025 02:34:04 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:34:04 GMT
ENV LANG=C.UTF-8
# Tue, 02 Dec 2025 02:34:04 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 02:34:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='b44fa2d67d24735bbcd2378df77b3afd2c5313bd275072e7d328718e2ce3fb11'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='dd0c4a9fc8008b0aeacadecd8df3373b395ed4d4d3fac501218d512ca509d178'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Dec 2025 02:34:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c884759da3effd451d2556fc8031e74f46acd6ddc0ab029e30e75b952478af4`  
		Last Modified: Tue, 02 Dec 2025 02:34:40 GMT  
		Size: 3.9 MB (3851349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6c50e8a499af9e80575cb4be765933a4376836ad558ae4b0e75cabaa2fee3d`  
		Last Modified: Tue, 02 Dec 2025 02:34:33 GMT  
		Size: 225.7 MB (225701225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:db953b7e1ebe865892640178da07ff48e29c13db88bb0d92304cfc08a9187a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9a5ff0774c3b8ee60517df99b52528d4e3eb82bdcc30a78c203a0cfa1f27c5`

```dockerfile
```

-	Layers:
	-	`sha256:091dd4858bbf017d8e34c686453d175ba7fbd138572171413792aef5bc31ee1b`  
		Last Modified: Tue, 02 Dec 2025 04:24:20 GMT  
		Size: 2.6 MB (2649423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec7cbca88185f85b8cd75d80633f424889c80b61218e7ebc43bc1fb50103cc3`  
		Last Modified: Tue, 02 Dec 2025 04:24:20 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
