## `openjdk:26-ea-32-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:074980a29db62472268bb4228b0a292e2af794d2a7e940c2d9710546414f9ea7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-32-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:241a41f3ded7b8596995bee059f56a06a9ee6d4b90db444c27ec292ad9c025e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257914472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8219ed69151d89ea6c7f0a3e9c609e345f197bfb6227604c436884e7d43334`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Mon, 26 Jan 2026 22:09:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:10:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 26 Jan 2026 22:10:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:10:11 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:10:11 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 22:10:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='99e956807a500a396bc799f5b450e79c295bccece78ae9ca67f3e75646d3a099'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef6d53835db7740daeda9be917698b14f742df288966e4985504f7f2e465ad0b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:10:11 GMT
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
	-	`sha256:f7028efea991849d4922f1cc87a16a50be2da896f3a6c94904eb47be710b9295`  
		Last Modified: Mon, 26 Jan 2026 22:10:37 GMT  
		Size: 226.0 MB (225954574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-32-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:23acfd67df831f19554530d71761220134b0a8680875eec287824d132f62f270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49370608060d5e456b04d8182ab0ff487b92411fc98cfe3d959e955465a8001c`

```dockerfile
```

-	Layers:
	-	`sha256:a5ce244664bd53bd4e9b0d280da78f5c24f9e3440258d8fe6638394c6202d93d`  
		Last Modified: Mon, 26 Jan 2026 22:10:32 GMT  
		Size: 2.6 MB (2649433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd9b12995f0b2b3e20515b30ed7e56c6b46ace31400971526dbb7e1eab5ee036`  
		Last Modified: Mon, 26 Jan 2026 22:10:32 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
