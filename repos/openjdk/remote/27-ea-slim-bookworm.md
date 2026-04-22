## `openjdk:27-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:aaf21555929234c7641a6d87f24af6220718c34a3458e4c026cdf86288fba25a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:66c3117efeff8fbaf95e90e3bfafcd98eed461ccda412690bc721b40a584d66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261059166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef252843a8d0af1b1bb19b33a855435fc6b32becf495163b3217adb511e3d92`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:45:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:45:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 22 Apr 2026 01:45:56 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:45:56 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:45:56 GMT
ENV JAVA_VERSION=27-ea+18
# Wed, 22 Apr 2026 01:45:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 22 Apr 2026 01:45:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a81a6b0e2746b9cb4f89e551b8a176fb302d40dddc76f03a80ef89d2480620`  
		Last Modified: Wed, 22 Apr 2026 01:46:14 GMT  
		Size: 4.0 MB (4030651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fbd0d8c23b01c2b56d26c998bd4650d860076ae7c3e5c5c9d79054469fc66a`  
		Last Modified: Wed, 22 Apr 2026 01:46:20 GMT  
		Size: 228.8 MB (228792263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:5ade4f87abbc8a08a479a103a75d733bdcc7209e21a011e8a032c9c2d0f25226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a69e7b802ddf4db6c1a31f80cbf6955301bb3e6d1de3fafefa501dfe0d3d308`

```dockerfile
```

-	Layers:
	-	`sha256:48d50ab7b7aad7db6f4eeb1550a4c4232d8e392851ae6ed434ddf12de0290f16`  
		Last Modified: Wed, 22 Apr 2026 01:46:14 GMT  
		Size: 2.6 MB (2648537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009228d8893e090fba15cdd8f3278e59ff9a8ebaab44ed56cf3ffd708053340e`  
		Last Modified: Wed, 22 Apr 2026 01:46:14 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:315f23a2383aee16b242e68a26a78a99a7c0a79a5da51a9c98cb9d4df028b671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258714121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a168118d394576af01583cdcf4f5c78e837e33e50924e6f33a442890714a5d37`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:48:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:48:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 22 Apr 2026 01:48:45 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:48:45 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:48:45 GMT
ENV JAVA_VERSION=27-ea+18
# Wed, 22 Apr 2026 01:48:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 22 Apr 2026 01:48:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef92e304ff893ff9651ddf90fc8ebc2891cc7dffcd6b22b6a9f5a94973d0ca25`  
		Last Modified: Wed, 22 Apr 2026 01:49:06 GMT  
		Size: 3.9 MB (3852222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb2a1f920d17142e71fb4e7d49f5977a464891de22566e0b95799c45325b92f`  
		Last Modified: Wed, 22 Apr 2026 01:49:11 GMT  
		Size: 226.7 MB (226745785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d4dd5d38dde8ddd975b7fe1d2f14c7680a43ef994e94921e465204ef994b725d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf8e10b82307395fb523021b370555e78973a54c3caa25caa49880b2cb6bb27`

```dockerfile
```

-	Layers:
	-	`sha256:3c2054806d7a638e979d11f603b8bc0fb92cb0d63faf2d30ab415c302edaefef`  
		Last Modified: Wed, 22 Apr 2026 01:49:06 GMT  
		Size: 2.6 MB (2648171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18670fb53f35a20ff20708c02a2acf9d9befdce43fd6196b7dc198f950264ae5`  
		Last Modified: Wed, 22 Apr 2026 01:49:05 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
