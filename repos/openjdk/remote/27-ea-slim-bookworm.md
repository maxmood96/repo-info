## `openjdk:27-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:e8cc96ad0ba727917d75a3ee09ef54f52cde813ef53c6f30e79bfad7476f4b2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:73c532c6107048cb489f6e4de0bb6bb137905435064ba5d9c94de21264bc94e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.6 MB (260642941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ed5949c426395ff8601ab822152f412af820fca3ba82e484f36d08632185ac`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Mon, 26 Jan 2026 22:12:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:12:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 26 Jan 2026 22:12:35 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:12:35 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:12:35 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:12:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:12:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd98f94773024a552fd24072b9af5779928097ad63b33461d0404f15f3de69b`  
		Last Modified: Mon, 26 Jan 2026 22:12:57 GMT  
		Size: 4.0 MB (4028170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656ca7d9bbbf62dec17e68457c5dea4a9a21459fd71d136e17b77021027ad28b`  
		Last Modified: Mon, 26 Jan 2026 22:13:02 GMT  
		Size: 228.4 MB (228386199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:22774de194ec1831ae963190766b70181503fe7377f29ac78cbbc70b0cc6ab71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf08b228618ab7aa3748d8f3e31f2457c7eca0821d6c8ad4af92b092b75cf89`

```dockerfile
```

-	Layers:
	-	`sha256:b7f9a2c96691936846b89d263a4803837cffdabc67293a94b97449944063c4f5`  
		Last Modified: Mon, 26 Jan 2026 22:12:57 GMT  
		Size: 2.6 MB (2649791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7174701b25606e5a26cf38259dd0de04b1332c8dae54edb15a502bf1cf247b8d`  
		Last Modified: Mon, 26 Jan 2026 22:12:57 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f49a19d7fc8eb989d355b139ce06e07e12d59c470ce9cd80e8c5799f30b8ac53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258269617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585341dcbc42ad8f98838be437ca7645505e331e21457af661e682a02f411f49`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Mon, 26 Jan 2026 22:09:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:11:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 26 Jan 2026 22:11:03 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:11:03 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:11:03 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:11:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:11:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cc23bab109a5236046cb013ba7ca55a05de6ccb93a2c2daf4159b0bfe38447`  
		Last Modified: Mon, 26 Jan 2026 22:10:32 GMT  
		Size: 3.9 MB (3852009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6074cad4376dc5ff8b049ea60c458eb7029741e0f1adbb5101d7c48d1df9bc`  
		Last Modified: Mon, 26 Jan 2026 22:11:28 GMT  
		Size: 226.3 MB (226309719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:87b90b616c972a4b67c4559c14d600e12313090b31c17fc8f1a615f4dcf1521c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfb384b2bf09157c7e919ca6fa9e6f747fa3c1d3f82f90bf81611ac3c137df1`

```dockerfile
```

-	Layers:
	-	`sha256:17f56b3b365d63a3ee79c0bb06e43978bc974ba53c6289de90dbe533c19adaac`  
		Last Modified: Mon, 26 Jan 2026 22:11:24 GMT  
		Size: 2.6 MB (2649425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eee02702d4026b45d4f6fabf986eab21a969f3de61a22737547e7e95d3aba1c`  
		Last Modified: Mon, 26 Jan 2026 22:11:23 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
