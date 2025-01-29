## `openjdk:25-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:22829103f81f65dfc507e0c6bf26e06e035c57c390138816d787cb2fbe2aee3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:bf44a8f61a67fc705db26f55b2c12025d674e234480cf00183dc01ed70935b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244090487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3004ab8dccd3d57b205ab099cfa5aab17ad235a92e12fe2c6f8b8d7815c2c3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 25 Jan 2025 01:52:19 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:52:19 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_VERSION=25-ea+7
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='7feccd12886711c8902b12a7af32cb26a34993f148b00a36aa93068ce1e3b128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='8f29e5e012a3477812ef892a16022af8410235782f12c41d09d2a7082e20849e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1569e59eab13f6230bd0338294f1fb09fceae3a81c5f2c7bc9ac9b246b65cde7`  
		Last Modified: Tue, 28 Jan 2025 23:28:18 GMT  
		Size: 4.0 MB (4018431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9f6ef1d0ab33ccb66e7b85253cb58b3bf595bd4f8a584d43d22a334604b19a`  
		Last Modified: Tue, 28 Jan 2025 23:28:23 GMT  
		Size: 211.9 MB (211859639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ed9af62ba5cf8b28938b381392b9e08994928c5f79ea2eadf61da84464369be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9635c21265c86d7960192fda17a4249ae4d8a84982866afe13c90af7e03334c2`

```dockerfile
```

-	Layers:
	-	`sha256:49281af12d06c6c39c3bcb5b7a6d8b2908a696341e605948b37ed4c42d704d9d`  
		Last Modified: Tue, 28 Jan 2025 23:28:18 GMT  
		Size: 2.5 MB (2533878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f8d527df540ed1b14bc32c9482f7440a77988fe6c0120cf9e45e6f5e4af58dd`  
		Last Modified: Tue, 28 Jan 2025 23:28:17 GMT  
		Size: 19.4 KB (19425 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:772cab2fc76fcabd69beb00406a87495855295ddb620714841b7c7b21eb8ada9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241704548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b458be1af07d038f53077a0a2e948f3566cb4942136a6f1a91c4fa545975c3af`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 25 Jan 2025 01:52:19 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:52:19 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_VERSION=25-ea+7
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='7feccd12886711c8902b12a7af32cb26a34993f148b00a36aa93068ce1e3b128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='8f29e5e012a3477812ef892a16022af8410235782f12c41d09d2a7082e20849e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f083f07e13bd63cd44a785caf631d4e023799e01a18898c1a673879d76b06aa`  
		Last Modified: Wed, 22 Jan 2025 02:34:57 GMT  
		Size: 3.8 MB (3833715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280e0467d24ae8d2e30ba72d89256a25ade0a3683e753195df1832a218524a3b`  
		Last Modified: Tue, 28 Jan 2025 23:34:59 GMT  
		Size: 209.8 MB (209829802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c08e2bea8053b0058173764ceeba97534a03112fec757dff24df2ae6c6be2e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e285233c8d4899f74cc5d53e787741509a954ae4843c56674b2313a954f22cb`

```dockerfile
```

-	Layers:
	-	`sha256:219061e63cb4331d07cccb3eb354f55ddfd2dc849d72535c4d32083f53b528f0`  
		Last Modified: Tue, 28 Jan 2025 23:34:54 GMT  
		Size: 2.5 MB (2533608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e035fac7707fd150e01b46b8372cf2f886d539339f58f49025719dfc4f40919`  
		Last Modified: Tue, 28 Jan 2025 23:34:54 GMT  
		Size: 19.6 KB (19640 bytes)  
		MIME: application/vnd.in-toto+json
