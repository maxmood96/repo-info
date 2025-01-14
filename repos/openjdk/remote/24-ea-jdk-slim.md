## `openjdk:24-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:89530e185e8d3880d339ee038c21b78accc61ff4f8456e5a5e1fdf3e3a5f3d68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:961204861d4d0247531642194672c3a8799a2e7f0d0be6138d40562c8f5597db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245148394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f87bb9af37f3cc35b69b88c42dd71942e13b83f6e9ee6fbbabdf663b78b294`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Jan 2025 07:48:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 10 Jan 2025 07:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_VERSION=24-ea+31
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='fc69771e3af411ad5be33bf328a73b32318264a7aef1f28d1e6339cbf609819b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='5c35cd6370cdbe71bda96ccae35f3a74972b83dc6958e783b803f730b24f9a0a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e443c8297581ebac251c68ab348e5b36b014095c1f5b2a1b4cc442efb65f3f43`  
		Last Modified: Tue, 14 Jan 2025 20:39:21 GMT  
		Size: 4.0 MB (4018446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526739855abeef76533d2412798e3af2bfba4782c58fbc9687fab5903ef333a8`  
		Last Modified: Tue, 14 Jan 2025 20:38:45 GMT  
		Size: 212.9 MB (212917531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:c058b322246dd23b743149ea4e32f076ccb0fa9d51d078194b85e0e17ff88ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea37f76dfd554ab0792f45773ff451d0d1a4564e17c5d74daa8992152d04000`

```dockerfile
```

-	Layers:
	-	`sha256:1718f274ad1e46e230c6c8fde44b537972c73d04d6ac08048186f31148f312fa`  
		Last Modified: Tue, 14 Jan 2025 02:37:04 GMT  
		Size: 2.5 MB (2534519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d50167ebca28c2a53558af5b3640b1160d820c012309f2ecb51d5623535316`  
		Last Modified: Tue, 14 Jan 2025 02:37:04 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5c8e7d45ce305e5ae386baeb71ed2420384280139ed17a96289bc0477e90b781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242758207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d2e44e9629ef314da8605014d410651d3a7afa4daddb3d99517d2bf092d99f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Jan 2025 07:48:13 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 10 Jan 2025 07:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:48:13 GMT
ENV JAVA_VERSION=24-ea+31
# Fri, 10 Jan 2025 07:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='fc69771e3af411ad5be33bf328a73b32318264a7aef1f28d1e6339cbf609819b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/31/GPL/openjdk-24-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='5c35cd6370cdbe71bda96ccae35f3a74972b83dc6958e783b803f730b24f9a0a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e33f314e8fb2cf61d9a062d3b34d4767a526de678ed71addfa16d440e763fe`  
		Last Modified: Tue, 14 Jan 2025 07:43:52 GMT  
		Size: 3.8 MB (3833710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0f69a2b2e95535a32fad87c1576b8e011afdcef1b2d81b19a4e4f3aa63cdeb`  
		Last Modified: Tue, 14 Jan 2025 07:45:51 GMT  
		Size: 210.9 MB (210883466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:1f3977e59d11c8eb1a80678eae81c0d4901d23fdc5a06fd4aa783cd8723eb838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b4f8c150bbcca18ee4752c13757fef4183cb9e128b5e00748511782cb977eb`

```dockerfile
```

-	Layers:
	-	`sha256:91cb8ee4d7b1ad6c435e59b2000e5b24a8fcf952225c44d0467afc46bf0a8b5f`  
		Last Modified: Tue, 14 Jan 2025 07:45:45 GMT  
		Size: 2.5 MB (2534249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e813150b330ee3dafe5d64b7f34090d78073e57b23f191f2ac4b5acd6dfef725`  
		Last Modified: Tue, 14 Jan 2025 07:45:45 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
