## `openjdk:24-ea-1-slim-bookworm`

```console
$ docker pull openjdk@sha256:216e2af9c34af0490cb6e6b8c5558379399bf8f515ab221e4f8475182c12a9ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-1-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:4e1e44065b0fd8a7a35e78c9a24638fc6144a8becf5d5d26bed9a6953cccfdd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244480707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2931fc0cd46f9ebbe11d33822eb661bde1444d00422be00834100e608cc4b3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 11 Jun 2024 06:58:53 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddf1e783af5d1a866183ded0960582a942701edaaccda82aaaa430e9e255b60`  
		Last Modified: Thu, 13 Jun 2024 18:29:33 GMT  
		Size: 3.8 MB (3821802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5376a9d7b7d436b1c433726b9e5118b5d61b8fb2faca445529b1f7fea56ec4d7`  
		Last Modified: Thu, 13 Jun 2024 18:29:36 GMT  
		Size: 211.5 MB (211508475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-1-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:bec411de0a08ccf002c5cb1a304a153bdd05ed8e07bf08d0679ba4a47bf5ccbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70325b711703d26bf629b36d44fa9ae2557508d7c7f5f5cbed7e1f8df0c53b4f`

```dockerfile
```

-	Layers:
	-	`sha256:a44f886f1665da4f4a1fd478364f62580b47129fad3347f4fd2d6cd31bb8eea6`  
		Last Modified: Thu, 13 Jun 2024 18:29:33 GMT  
		Size: 2.3 MB (2346302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:053c8462487f02dcf5aa072eab3150984bfe9c3f91eac392db78df391654501a`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6adab604a2d04fdf584901a95b33ecd97ce3b9a962b8b62c456764fa3bf372bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242193551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c15e8da17fb854e45fef6028ab0404b603850e32e60637c4167ec6ea3ee24d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 11 Jun 2024 06:58:53 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb960144e9a3234b18ad0a695286d60905b47d016807f2c30ce00e0acd5b3ab5`  
		Last Modified: Thu, 13 Jun 2024 19:56:32 GMT  
		Size: 3.6 MB (3629819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f871202774e5570cb9c2c1a5eb274aeb530dd57692df8930d5cdc4e4abbb5537`  
		Last Modified: Thu, 13 Jun 2024 19:56:36 GMT  
		Size: 209.4 MB (209384066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-1-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:713a2a25d25a0e75a170764eb403544ab0091236154b5dd372b7b087bd91a98d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612a3b1a7aec31c44eeab288d36091bc05f1729916b490435837f36645421d98`

```dockerfile
```

-	Layers:
	-	`sha256:d94887917d9200b4137525c215f39a51905771b1646035f53ebd61fec43ffee7`  
		Last Modified: Thu, 13 Jun 2024 19:56:32 GMT  
		Size: 2.3 MB (2346656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f99c8a3c8f5e8cc0e05941d18790cc92e2d4a9266eb7fbb4c597f1ff57aebeaa`  
		Last Modified: Thu, 13 Jun 2024 19:56:32 GMT  
		Size: 19.6 KB (19618 bytes)  
		MIME: application/vnd.in-toto+json
