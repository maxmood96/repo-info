## `openjdk:27-ea-2-slim-bookworm`

```console
$ docker pull openjdk@sha256:ee679fd5df65aeafd41cb0f07a5ae2120f1db4c2981e33b914d79caa511c13d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-2-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:e534f449e86705afd475b1b32a29361e591cf5d0846ae4a1dafb4812d7b4d1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260430820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955f66b4bf0daf364e5e76d466cd917f4b41388e1be73eba2120799334d70e80`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Tue, 16 Dec 2025 00:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:02:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 16 Dec 2025 00:02:58 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:02:58 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:02:58 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 00:02:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='95b0225ac04e0034ffe1626daf09cf436a54ac3b74fef67ccd00534beb7715f5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='111a65a5acf09c18b471be75d77130d10b4c425d192ae243e3940da32e5d6dca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:02:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547ed68598b6fcdf09dd719b6ce68b727b5cbd8454007d296f6e4e8b7b68ab76`  
		Last Modified: Tue, 16 Dec 2025 00:03:36 GMT  
		Size: 4.0 MB (4027343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a83d9f0e3a1bb673719918c3937334471b192d76454cb9d4b206e2149ac3fe4`  
		Last Modified: Tue, 16 Dec 2025 00:05:50 GMT  
		Size: 228.2 MB (228175059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-2-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:bc5204c4773993a8288c762651065e276a82aed88e053209eefb8403548461a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d18f60ae14b1e5d0e1bb33115cf78c27e497c742e79c0685cd93f7107e84f0`

```dockerfile
```

-	Layers:
	-	`sha256:23156d6b99a101b1c583abcbe7a5185e7f3471857ec08fdd9d9f9b05e2f027b0`  
		Last Modified: Tue, 16 Dec 2025 01:26:26 GMT  
		Size: 2.6 MB (2649779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876aaacacc8ac6c314acdc658483de7aa704f49ebb9b846340563999cd684d37`  
		Last Modified: Tue, 16 Dec 2025 01:26:27 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4ab842d544e5594b6cbd813f61b8c22cde6f656a5f578f9b74a5a5b9c2deed6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258058456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892e2399844980d04c4471303ddb187620c6901d2238f3d4e01866a54f24fbfa`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 16 Dec 2025 00:03:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:04:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 16 Dec 2025 00:04:07 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:04:07 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:04:07 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 00:04:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='95b0225ac04e0034ffe1626daf09cf436a54ac3b74fef67ccd00534beb7715f5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/2/GPL/openjdk-27-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='111a65a5acf09c18b471be75d77130d10b4c425d192ae243e3940da32e5d6dca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:04:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e876004ac1f55576e9071348072268bc0ee7ad4f84fa453bf2d390127e0cb8a3`  
		Last Modified: Tue, 16 Dec 2025 00:04:39 GMT  
		Size: 3.9 MB (3851404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7464aa0548f01fba00f74e84f63f79bdade181c49507c642da799171774b58b`  
		Last Modified: Tue, 16 Dec 2025 00:06:37 GMT  
		Size: 226.1 MB (226104823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-2-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:cc1b96effb17eba546a3a0171814eab0ea9ba465ee9d66dea6f9aa5ca0ac9b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab4646c6289756d925bea691b53c98b161c2f8051fcc5953e31eeae6f2f1816`

```dockerfile
```

-	Layers:
	-	`sha256:f216bcb827b6aed0a24989359bb7c3aecddcf65bfa3282fcf0f8c95ec5856f22`  
		Last Modified: Tue, 16 Dec 2025 01:26:31 GMT  
		Size: 2.6 MB (2649413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c144cb6d3b2ed309fd8af3ffcd4af240939b5af0fb56d8d748a290809ff5a610`  
		Last Modified: Tue, 16 Dec 2025 01:26:31 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
