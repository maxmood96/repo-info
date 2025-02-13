## `openjdk:25-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:b370ed760de452077d4e991a363b25a9e63244d7f01957ac4b65fd65673aa9ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:527233aad996a6b2037f0c0df585a00fdf0d96a133aa18323748aa7f34c9c9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244210447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cc66c53c9bb5b3ceaad4bffa3d2ac9e25c73688d4a2adca5f7a6b9f695dc6c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 07 Feb 2025 01:53:06 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:53:06 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_VERSION=25-ea+9
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='7c57d59eebec0a42a9bca9611b79759eaaeee24f115a9503f4977e5f089eca90'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='7297335988877649a1eebd21261a54e3d96e4f82038766b1a8dfae4fc177ea02'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c30cb76d688738710b36676c06e40813b6b1054b9f863e27c69cb8ba4bca35`  
		Last Modified: Tue, 11 Feb 2025 05:17:02 GMT  
		Size: 4.0 MB (4018379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2cc3825f830f833a2cc662ef92b07a961f104fb93337addf6debe66393ee4b`  
		Last Modified: Tue, 11 Feb 2025 08:46:38 GMT  
		Size: 212.0 MB (211979765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:a67275edbb45c2ecf504588f4801b46a853fb51b9563ea592340b8891db0b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2557063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7235f7ff2692ae3d690e9ec63a191f09cc284c2f0deb2bc11536e2be59ef964`

```dockerfile
```

-	Layers:
	-	`sha256:09cb880b8ea63f9a1ace59114a0d45a73c1513ab2e7bc3c89de31330ee292861`  
		Last Modified: Tue, 11 Feb 2025 00:27:59 GMT  
		Size: 2.5 MB (2537638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8df33a79496fc789a99bfae0a1731d844fb3cb89270276cf06d3a6298d174104`  
		Last Modified: Tue, 11 Feb 2025 00:27:59 GMT  
		Size: 19.4 KB (19425 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ae1c4a66977857f062e74322bea8fcdf79856f88bd42e79ed67787668d056020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241827283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0797c0ed138f34d028ae80f4c2d4adb65e126d8f413a0af25ff7a8d99bb37b5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 07 Feb 2025 01:53:06 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:53:06 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:53:06 GMT
ENV JAVA_VERSION=25-ea+9
# Fri, 07 Feb 2025 01:53:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='7c57d59eebec0a42a9bca9611b79759eaaeee24f115a9503f4977e5f089eca90'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/9/GPL/openjdk-25-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='7297335988877649a1eebd21261a54e3d96e4f82038766b1a8dfae4fc177ea02'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:53:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43b4f96d2c0ec3b3b9b795e151e48b648a3451851e1ceb16e34f7cb4fbebe83`  
		Last Modified: Wed, 05 Feb 2025 06:59:29 GMT  
		Size: 3.8 MB (3833699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e077c5399ce787bb7ec11cb6d311e6b11d78d1154cf9345cccad66ffe1cfb43`  
		Last Modified: Tue, 11 Feb 2025 09:44:56 GMT  
		Size: 210.0 MB (209952703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:81b66ddb388336001b5b8a6dcfb0830935a6d8758de950b544e513c1ec1f75b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2557008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db0494c6d47da5f6964065d9c51d99eeb2c66ffee5f6c8eb8daedde14afe5ff`

```dockerfile
```

-	Layers:
	-	`sha256:61ee4bc9279b31bbb0007d888b48d517a3e3d1638da3d7cb4cba99724528cfa0`  
		Last Modified: Tue, 11 Feb 2025 00:36:40 GMT  
		Size: 2.5 MB (2537368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2022352e31863aac46c2eec9bfdf06b0063aaa0120d4ac0d3d9da7778c4b772e`  
		Last Modified: Tue, 11 Feb 2025 00:36:39 GMT  
		Size: 19.6 KB (19640 bytes)  
		MIME: application/vnd.in-toto+json
