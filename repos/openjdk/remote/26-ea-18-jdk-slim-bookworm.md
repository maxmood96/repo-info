## `openjdk:26-ea-18-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:c7f31ce74bb3be9a8386191cf63ff300e9834c5298b638c3ecd47852b838b076
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:26-ea-18-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:361e3ae56e9bd9753bac9f55f4e7e15695bb5796c6ed33d0af23e31a6d6ce7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258086552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3147a4a4030f1d0eb7b00bc80f9776cb9c2dc75e9868a142bc0717110d6e3b8d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 04 Oct 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+18
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='efaa7c08b216ca30d5769c56a81337742b795188f8ab45532f711cd0fedd7971'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='2176c4bff69a4a7825dbbd296ac2ab318460f5dfe104d5590be6f3f470d7dd5c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614cb486d89b8cd8559cca76733cdd3da61f121b62c62091437802cafc64afd1`  
		Last Modified: Mon, 06 Oct 2025 21:06:03 GMT  
		Size: 4.0 MB (4027297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7c56565f62cf1eab590bbd948f10848222409ac42774054baa0007c18d3db2`  
		Last Modified: Mon, 06 Oct 2025 21:05:53 GMT  
		Size: 225.8 MB (225830919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-18-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:5cc3c778818b51953465ae1dc5953fbc94891c9becdd582ad43a92d7cf805681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2670518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c293daaf552698e5ae914f31213eb2f4399db127ef3bbc0107a9983198580fd`

```dockerfile
```

-	Layers:
	-	`sha256:f48c7f9e9d29ef24218d00a259d2ae2f0aee025b7b70cda27de082ffdcab5eed`  
		Last Modified: Mon, 06 Oct 2025 21:24:04 GMT  
		Size: 2.7 MB (2652948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80d4bf474fa29af1c71a011daa1f243882b7640ce81a8d6f05c1bffa57243d7c`  
		Last Modified: Mon, 06 Oct 2025 21:24:05 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json
