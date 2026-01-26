## `openjdk:26-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:aa1843faed9a33046e8bb74e946ab118f27d29aa102a2a0ceed9da7c0638e127
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:55d653c58a4d46db43b00ded6d41478b802d5895f5581ccf1ebead73361a1e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260267260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438a3e6b4cd9f74ab187b578bdd1ac0ebc2ef5750298b0a2a1bc7756321b2f6e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 20 Jan 2026 18:47:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:47:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 20 Jan 2026 18:47:53 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:47:53 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:47:53 GMT
ENV JAVA_VERSION=26-ea+31
# Tue, 20 Jan 2026 18:47:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='bfc006ca65cf590a40d808e5dc5cc973b98e11e309d0efa5dc36340c8b3ffdbb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9511be1b72db3be1c49c25cbecda90f37642003c9844f7d363455ad702ff7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:47:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8600b4836437ca053b688daec2dcd773a2734a8dd46efe2ec673f501265ac1`  
		Last Modified: Tue, 20 Jan 2026 18:48:14 GMT  
		Size: 4.0 MB (4028180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267cd9b7364fc71975c690579216e9ed0950cbff2afbe8bff932150b53364f5d`  
		Last Modified: Tue, 20 Jan 2026 18:48:18 GMT  
		Size: 228.0 MB (228010508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f1e12312c20fab75a497dbac644499fd39cf289283b6b921e9402e892188cac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa82f6d71230b6c1543ccf00bc2ee283747d49124f44e56a18d443d0db9e8d36`

```dockerfile
```

-	Layers:
	-	`sha256:b3142644232fc2af29e72a390b887b74128bb8e76125dce140634161696eafe4`  
		Last Modified: Tue, 20 Jan 2026 18:48:14 GMT  
		Size: 2.6 MB (2649799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:444db168645e89e21db8501d3384eb336e54766403db8d833c1b9bb99d88f3a2`  
		Last Modified: Tue, 20 Jan 2026 18:48:13 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim-bookworm` - linux; arm64 variant v8

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

### `openjdk:26-ea-jdk-slim-bookworm` - unknown; unknown

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
