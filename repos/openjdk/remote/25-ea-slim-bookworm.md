## `openjdk:25-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:12f768298abadd526e00f544f2eed496af78dec0b2870cde7683df47600843e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:5b58e725315f762df89195179c0877d5426c9959a1af2d83b42d9a02ba29d161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255410066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a22314c15f6dcb9c1781560ce5efbd5f064bc4c25542580087434bf206f4a5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 14 Jun 2025 00:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+27
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='96753b911566d9a6bcbdc84cde764dad6ac5250976260bbd3af509765ddfc8bf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='d4dee2002500348945826f4377fe2b480b57fc39fe5ac9cefe09ee46f36fd2d3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76659df88a3d11b9ddac2878d577ad305e62c860a1d444f9ff34dc9cf4e0346e`  
		Last Modified: Mon, 16 Jun 2025 17:50:53 GMT  
		Size: 4.0 MB (4024178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b2eec6de9d25ab37d30f82c05c164d83966d7f91e21d1935a25e4cd7bfefb`  
		Last Modified: Mon, 16 Jun 2025 18:28:20 GMT  
		Size: 223.2 MB (223155759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0c9b89c54b430b6352539d4d31b10edf804e2aa460eb0f600bc9a9390d19a883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2672777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8022251f47c6d85cfa15ca6808a7ee963224487b58ec655fa8983010eadc217f`

```dockerfile
```

-	Layers:
	-	`sha256:171d88c3892c393c5f30a2d789e51f97cfd8659e49475ef7795d091e96eb20f5`  
		Last Modified: Mon, 16 Jun 2025 18:24:04 GMT  
		Size: 2.7 MB (2653335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d39eccb3751247c01571ca108c13ca7dec0b25c9ce84d0db7684a3ef305a12b`  
		Last Modified: Mon, 16 Jun 2025 18:24:05 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7b6481df3947605edecf1ebabc1d5a74cd37b3a7cac32156a8a9b936f378081b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252844534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f4974d78b0d25fac44239bbe045fa837a6f4a51bc7811a5e6605abdbf78c08`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 14 Jun 2025 00:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+27
# Sat, 14 Jun 2025 00:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='96753b911566d9a6bcbdc84cde764dad6ac5250976260bbd3af509765ddfc8bf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/27/GPL/openjdk-25-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='d4dee2002500348945826f4377fe2b480b57fc39fe5ac9cefe09ee46f36fd2d3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e18990aa6eb4a8b7eff1a3a25d697c7e42c88ab4c53cdd37801790c34f6ec5`  
		Last Modified: Mon, 16 Jun 2025 17:53:12 GMT  
		Size: 3.8 MB (3836574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b181c489d89e0ee5af07e24fa7a5cff29ddf83e2e93660c440550393fa74590`  
		Last Modified: Mon, 16 Jun 2025 19:22:05 GMT  
		Size: 220.9 MB (220930285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4ce82814865e7f577a1dbaeff24c795b75a8c6467d16821dc9f778dd10d1d002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2672722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7cd51724a9c7407250b61c6797b848046fce51fc745994a604af5b3c8c79cc`

```dockerfile
```

-	Layers:
	-	`sha256:2c13ccae8f57bd99e2dcbba689dc3a7d89ad8c93318dceb67824caaadf82f45f`  
		Last Modified: Mon, 16 Jun 2025 18:24:09 GMT  
		Size: 2.7 MB (2653065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2eaf618ea93913840a7f3cac688c3a192662d430a8a68af7a6f8f6337c5f95`  
		Last Modified: Mon, 16 Jun 2025 18:24:10 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
