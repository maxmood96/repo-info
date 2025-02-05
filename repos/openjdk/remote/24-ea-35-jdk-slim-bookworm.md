## `openjdk:24-ea-35-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:181c65e6ee33b1293101ee81567baf19c8c5b44e148385e1b1143a6aaf866ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-35-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:5a1e04c65a8242e84cd113f0491715662450f50bbca079835f66afa6d6c67c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245238568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b49c2d713f334b0a8d76f7336cbd69b00e4cc727fac0b26148c8cebe8d32443`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Tue, 04 Feb 2025 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='bf5289b474e53b34a9ece42dcd3ae073e5ef7df63fcb9c44fbcac92496dedd99'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='96e6ce86751c7aceb6e5f435be31ecbd0629592097abbd67d1c0f5c5b85c8f78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084f4263b0081fac22e7a8ace1b27571f334d1ee8853ffcf9724057b6e4aeb95`  
		Last Modified: Tue, 04 Feb 2025 23:32:27 GMT  
		Size: 4.0 MB (4018426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551e58bd23cdc125d4bf1e1896abefc1a6c78e430d9b78b52ade4bfbf767a056`  
		Last Modified: Tue, 04 Feb 2025 23:32:30 GMT  
		Size: 213.0 MB (213007839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-35-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:6aef174058665c81df6224e02628b6e429ae7ec486bfe2985910b28982882616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2557721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3ddb50362ef0e66c5927ac1a6fbe02bc5e00378d2eab9b9bb91a7492880e89`

```dockerfile
```

-	Layers:
	-	`sha256:331f6634e7bf596c865eb6ce116d7d3d43759c75ea3b2ea76cd90388259402cf`  
		Last Modified: Tue, 04 Feb 2025 23:32:27 GMT  
		Size: 2.5 MB (2538279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba01fd3e4a63778ded036e2cebd49180c150a6967a2b1ea8c5e7cc17d1e8582a`  
		Last Modified: Tue, 04 Feb 2025 23:32:27 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json
