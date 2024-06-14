## `openjdk:24-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:8a4301d186040e7a7581a5445fb18008a36fdf100d0884d36a610653f2a5aedb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:42df41e77e8b944f67068666fd71409e3e7cb600d1d6eae7e67744e78c5952bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244314397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784f14013ecaafe86cb553c7fe48be79a695e62e99f0d2ae295c954c043bfeb1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 11 Jun 2024 06:58:53 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Tue, 11 Jun 2024 06:58:53 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 06:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_VERSION=24-ea+1
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='8548b9f8147e53846600a5afd39adb7f3f50a226edeb12e336d43837708f0dfe'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='d98e475916eb68814f1ddacc0ba56128025a829351b7bc51e4b4b862cf12d5fb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71baf5b7624bd9751eca35309a40e2b1780c23c59e3c3c722fece0b654c953e6`  
		Last Modified: Thu, 13 Jun 2024 18:29:39 GMT  
		Size: 1.4 MB (1378063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a41513c004d46e894c252451003a60c041ba05d148ec751830523003e796b22`  
		Last Modified: Thu, 13 Jun 2024 18:29:44 GMT  
		Size: 211.5 MB (211502294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:c75d8cd19594cd5e33dfc2622b6c68e27dd3057188385f8fc502fc02a3d30304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0bd21eb9678d9f70235e1c1508dacffbd06ae1704afd6e52f7552f2a8b1ebc`

```dockerfile
```

-	Layers:
	-	`sha256:bce6acd184b2e57805e41e9c74cb249446d408ca5ef303c21f8cba7d429acfbe`  
		Last Modified: Thu, 13 Jun 2024 18:29:39 GMT  
		Size: 2.6 MB (2638484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cddbe11dbc4c0576204cc838f452c7f904f41f48c81749feb1bbc4f93977e684`  
		Last Modified: Thu, 13 Jun 2024 18:29:39 GMT  
		Size: 17.3 KB (17345 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:932258df5d16a8daebb8c645211d343cdfded6ae57dd96a67138cea3e066feef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240831460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a408c17e7526df91710818742096d682afa135d3a35c8c1a2ca4c2f85b379ac1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 11 Jun 2024 06:58:53 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Tue, 11 Jun 2024 06:58:53 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jun 2024 06:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 06:58:53 GMT
ENV JAVA_VERSION=24-ea+1
# Tue, 11 Jun 2024 06:58:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='8548b9f8147e53846600a5afd39adb7f3f50a226edeb12e336d43837708f0dfe'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/1/GPL/openjdk-24-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='d98e475916eb68814f1ddacc0ba56128025a829351b7bc51e4b4b862cf12d5fb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 11 Jun 2024 06:58:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8abb9c6653ca6c247cb904f25b084470905f4d6682db52ade7c408705b3728c`  
		Last Modified: Thu, 13 Jun 2024 19:58:27 GMT  
		Size: 1.4 MB (1361905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35ab064231f490bb64f27b12069be314f31d5be88dfb1c4e84b8afebc7cdbbe`  
		Last Modified: Thu, 13 Jun 2024 19:58:31 GMT  
		Size: 209.4 MB (209382582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:1ccd10ef79a503442889c1d534726c6bf45996487fc89827840c0f6fae0751e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2656438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc703a11a6c6d924acbb6e9b27a7683945e3a1b91e594738e79ce256f9be13de`

```dockerfile
```

-	Layers:
	-	`sha256:d20ede8ad53567bd2774caabe83805ea22569e36ac638ce876c9686eace057ee`  
		Last Modified: Thu, 13 Jun 2024 19:58:27 GMT  
		Size: 2.6 MB (2638760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea92161cbf5db7efe01633ce239e716e02284630252678fa743dd0a5273ca15`  
		Last Modified: Thu, 13 Jun 2024 19:58:26 GMT  
		Size: 17.7 KB (17678 bytes)  
		MIME: application/vnd.in-toto+json
