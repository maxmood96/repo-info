## `openjdk:27-ea-jdk-trixie`

```console
$ docker pull openjdk@sha256:3b41691bacdd7dfb903b2bd2fae599b508678f593f2f52ba8806c762af1cf9dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:199580773200bdf53d82e6e53a1a5194da53c58249bf4e30e514ae99a4dc5b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.4 MB (387371155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81bb6e631af2151ab413384cf24758feda5327d6b91b2a7a75657c9708fbf70f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:18:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:18:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 08 May 2026 21:18:59 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 21:18:59 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 21:18:59 GMT
ENV JAVA_VERSION=27-ea+20
# Fri, 08 May 2026 21:18:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 May 2026 21:18:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf6c0a95e34418907d5abfe604d08c5cc6bf9d689943856fcd842eb2be82c6c`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 25.6 MB (25623106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a92b93bf7181c9d6b4525236a1a2fec85dc591d4deee481e828e707853f42c`  
		Last Modified: Fri, 08 May 2026 20:27:02 GMT  
		Size: 67.8 MB (67789206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f179fd86d47623d9ea3d27967e9395b31f9ddfc3d20037fff49868d8b77b1e9b`  
		Last Modified: Fri, 08 May 2026 21:19:23 GMT  
		Size: 16.1 MB (16065022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75052f9e8c2f778cbd8f869e745540ff0d1b17e5355cd4e24fbaa3ba109dca38`  
		Last Modified: Fri, 08 May 2026 21:19:28 GMT  
		Size: 228.6 MB (228591501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:0aa2af4254f249eb1a71bb37be16fe6452d9d64b7d837b1578f8ccacc29383a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b843710efd81a5b20eb221d20fae13eaaf3c9bc958543b6ad7f669da501982b`

```dockerfile
```

-	Layers:
	-	`sha256:8b3230fdb8b00c2a3c0ef12d1e1a427ec1d2602ee500e9abd68d163b0204abb3`  
		Last Modified: Fri, 08 May 2026 21:19:23 GMT  
		Size: 8.5 MB (8509920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:795a235af9797d6a87c8c7bf61c16fa7f873cd86bbe6f8a5446ce84742b4f495`  
		Last Modified: Fri, 08 May 2026 21:19:23 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f2bd865b0401e0a1285d3e831a3e52cc3aa9235ea9ef07e52706e70873736684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384912008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a54d970a82c5368388d36146677c08661a3fd735ad6dca43b1ce6c8f5fe509`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:18:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:19:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 08 May 2026 21:19:01 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 21:19:01 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 21:19:01 GMT
ENV JAVA_VERSION=27-ea+20
# Fri, 08 May 2026 21:19:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='a7c288898b71578ab424b0234102cb576ac5cf71c31bbdacc5d610a36be3d9cb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='47a8c6fedd9b292e5b5a5ad9e4cd238eecfc4d1cf098f052d48e7b6f19a0b025'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 08 May 2026 21:19:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6968d8edb06bcdaf22846e8626a2500d70d68bae3413bca896fefe955e2a6ef0`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 25.0 MB (25023476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc880ef5fbb726989fb57630c05c39cfe57a36a9f03c5b86a2d51c9c86ed66f2`  
		Last Modified: Fri, 08 May 2026 20:32:42 GMT  
		Size: 67.6 MB (67592055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aedd93dc5c805647fa90bdf7065c13ae4cbc7b2b9f22d0b988e3f784ec5701`  
		Last Modified: Fri, 08 May 2026 21:19:27 GMT  
		Size: 16.1 MB (16071215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2581a275c0299c6c6d81b0db27949c96027fbc8ef855162bfce7a552004b81`  
		Last Modified: Fri, 08 May 2026 21:19:32 GMT  
		Size: 226.6 MB (226555817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:777008706b1e541c229ae6fe7583d517f5cfad726e13db673342559e16051f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83ded624b2109fea42ecea613604abe3cfc4f9f8eca171dba4c09764598cb41`

```dockerfile
```

-	Layers:
	-	`sha256:fc8c4afaf6c3f110dec33e535fd73d217f29e064f124af52b195fdc15ffd3c55`  
		Last Modified: Fri, 08 May 2026 21:19:27 GMT  
		Size: 8.7 MB (8704710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16e75548a99198685493c0d1b8a33aa8f942636066045246cbb9ed546e6f0aed`  
		Last Modified: Fri, 08 May 2026 21:19:26 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
