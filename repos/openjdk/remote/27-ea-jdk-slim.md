## `openjdk:27-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:15bebdc25889629a32210499ad3bc43f2ba21254c89b2a23d6880e650a7ca3f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:2c18e6ab453cc2c017290a59a1f5588bb0be51911910a22d849baaa841763a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.3 MB (259272921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89157f8aaeae35e8d30abcc3e2e44af4e55e5a987dc14f9513dc43dd461b1e7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:47:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Thu, 11 Jun 2026 00:47:34 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:47:34 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:47:34 GMT
ENV JAVA_VERSION=27-ea+25
# Thu, 11 Jun 2026 00:47:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 11 Jun 2026 00:47:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b4f0f9021e28b46e17e6ef01f6419a2400a26339edd334c30fd7a1f9634ff5`  
		Last Modified: Thu, 11 Jun 2026 00:47:54 GMT  
		Size: 2.4 MB (2371303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b64dee2c73e0e06bb6a92ebee9991aae9776ea29a17caf6cce00f5a07412500`  
		Last Modified: Thu, 11 Jun 2026 00:47:59 GMT  
		Size: 227.1 MB (227116203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:f639408f0c9837c58e4747ae5d10e5abf872ea080ee9c70aecfa42f63858e892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5c7abc14688a0a5da3f7483dc4a0d5a518f3a33cd1588ad215dd041e7612e8`

```dockerfile
```

-	Layers:
	-	`sha256:5f62b0353922b0b27d2ca7bab75308fd5dd8a093adfb9cd635967d2624e1e309`  
		Last Modified: Thu, 11 Jun 2026 00:47:54 GMT  
		Size: 2.3 MB (2276384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e6ef922e6b579702141c2c6cd72b63c66e0d69eff132cc82ad05277d269ef54`  
		Last Modified: Thu, 11 Jun 2026 00:47:54 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:40b07bffacad2e8f01bfabf16e9b997e98717e53681367e0f671dfeaf10993a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257562144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b57423fd2290a8844df29bf43820276c5334982830e20e55e57ab490f9b69c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:49:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:49:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Thu, 11 Jun 2026 00:49:23 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:49:23 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:49:23 GMT
ENV JAVA_VERSION=27-ea+25
# Thu, 11 Jun 2026 00:49:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 11 Jun 2026 00:49:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dde28c6aaab33ed7332f6dda9ae821605f5f6bee8b50b960e5a1ed1909a6585`  
		Last Modified: Thu, 11 Jun 2026 00:49:42 GMT  
		Size: 2.3 MB (2314579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416c8914306b0a9cb92b8926dc532f768ce83115115b18133e44144737abaa3f`  
		Last Modified: Thu, 11 Jun 2026 00:49:47 GMT  
		Size: 225.1 MB (225099035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:9825ea880e7077c36baea7a3571323a82bce18d3b0f0c570553698099fd07829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99a2e825f145a26f0bae356cd2c55a2e739c924f832da85609ae24e92145b50`

```dockerfile
```

-	Layers:
	-	`sha256:2c75f7d09c441d5b7743cd4286e56e93d0013c10a376351d6621f9830219b464`  
		Last Modified: Thu, 11 Jun 2026 00:49:42 GMT  
		Size: 2.3 MB (2276062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f460ed661291f66369a3d126b0e74e75a9c917a6106fa8424f09caab3898319`  
		Last Modified: Thu, 11 Jun 2026 00:49:42 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
