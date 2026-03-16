## `openjdk:27-ea-13-slim-bookworm`

```console
$ docker pull openjdk@sha256:81d71063900f13fcbab245a8e75a744779f5f8d74a5ab55a2797811588c69dff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-13-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:bcd0349da60cdfe439cdfc2cf8837f2d3855022ba3e805a469bcfcac544ea790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260873643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c315cb5cc00630d36b52d679b0095f3b95cb1b2a79d98172f1baf6a8c65dbf20`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 16 Mar 2026 17:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 17:03:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 16 Mar 2026 17:03:59 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 17:03:59 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 17:03:59 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 17:03:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 17:03:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d595c0d807073962219aa263a92949a5fca8923bdb19fa97293566627b1247`  
		Last Modified: Mon, 16 Mar 2026 17:04:20 GMT  
		Size: 4.0 MB (4029231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14ce76b6ec7f7bd9fb092143717254ddea09fb4848109c5261ffa9fdca6cac1`  
		Last Modified: Mon, 16 Mar 2026 17:04:25 GMT  
		Size: 228.6 MB (228608133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-13-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:15122068260ea654d27a227bf13367c0ed10037b886dd2fc4c6377e0fbdf5a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5857226ed6fed81332b7b951235c45847ce46f285ed4d26b87cfc8b314e36f08`

```dockerfile
```

-	Layers:
	-	`sha256:6d9dab0d1d9acdac52f0e0b950c4715ea20f1ac181c5f990cd8c1d6ba7b95936`  
		Last Modified: Mon, 16 Mar 2026 17:04:20 GMT  
		Size: 2.6 MB (2649807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f7688539d698911e8e9b997d9254cadc553d1a3c68f2371390390e76bde1c6`  
		Last Modified: Mon, 16 Mar 2026 17:04:20 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-13-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:41f564ba6a9f1896d974da4ba11c782df99d828d2c24478b26bd44bc892fca47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258535542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87092916bbe577054be5fb38c14d52f40795b0355496e17ee0fa91057f1f5f8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 16 Mar 2026 17:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 17:05:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 16 Mar 2026 17:05:15 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 17:05:15 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 17:05:15 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 17:05:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 16 Mar 2026 17:05:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71d2675e70e4a98170fc061be69c270d01127cb1d331df82f7f800662f6e5e3`  
		Last Modified: Mon, 16 Mar 2026 17:05:37 GMT  
		Size: 3.9 MB (3851967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffb9e0c6916ff242ccba07a4e09a951fe8c289f3544979cc5ca2da177742acb`  
		Last Modified: Mon, 16 Mar 2026 17:05:42 GMT  
		Size: 226.6 MB (226567494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-13-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3ff008307543d7f05144fa9af9a93dba2f3c11055119dc35cfb2727afd4e831c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07725f4b68dda203225f235da0e34ecb3ff605dbe5e157920bc789d4eba5db8a`

```dockerfile
```

-	Layers:
	-	`sha256:9a09fd181af9ecc07d1a2e7ee03e4b92bb858e2a013b5d470354b366123e0b85`  
		Last Modified: Mon, 16 Mar 2026 17:05:37 GMT  
		Size: 2.6 MB (2649441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc797a82c4d8a13c668d7283742cabb60e76074578110becaec7d3416564e859`  
		Last Modified: Mon, 16 Mar 2026 17:05:37 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
