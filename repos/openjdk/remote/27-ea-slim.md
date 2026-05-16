## `openjdk:27-ea-slim`

```console
$ docker pull openjdk@sha256:674ea3bb230f5cbaa4886173ffef7c79e8fa83c0fa85dfa89042e041c2cc8aed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:dd09edf67abb7a005025fa2c7d722eaaaccd60b207520b0ee1d8f7199102982a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261122747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073af7016ff51adcffaea328ee18dcaec0980629d43f3a3b89ed6b5b5c15f48`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:18:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 20:18:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 15 May 2026 20:18:42 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:18:42 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 20:18:42 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:18:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 May 2026 20:18:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c7c75f27d3027fc7277b04e3a650e2a40906c184e033ebf5c8283dd3c6f811`  
		Last Modified: Fri, 15 May 2026 20:19:01 GMT  
		Size: 2.4 MB (2371165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf63dc636cec19b70f575d47f4abdd54a2c4b18af8bfcc01bbdf279735e38333`  
		Last Modified: Fri, 15 May 2026 20:19:06 GMT  
		Size: 229.0 MB (228971356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:dbcffd88afd7de2f9ac8eeb5ba1cbddf75c5e24dfcce5f4a28e96e6ba7b657c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6162dbff14c99207daae7cfc02b4caab7886d33dd416cf07885abace6e6f8d65`

```dockerfile
```

-	Layers:
	-	`sha256:b2c070135bbdefe73c0e34b5cfc94096d7314f2e6380d19e534c0a76395ee139`  
		Last Modified: Fri, 15 May 2026 20:19:02 GMT  
		Size: 2.3 MB (2277625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2846c878931a16a871ea25603f50e8fd078162ffadb890cb5ca136548492b5`  
		Last Modified: Fri, 15 May 2026 20:19:01 GMT  
		Size: 18.1 KB (18108 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:80e03e6defb6e2c62053055e9c22235d53b7790aeb9556bd105f208e85510ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259389055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a215a4ed1e55bb0575d55e5bc0ee9ee4ce5ae3446eed69c2563b37a19cff12`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:18:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 20:18:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 15 May 2026 20:18:27 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:18:27 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 20:18:27 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:18:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 May 2026 20:18:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e92971cbec32035b5475e8f3bc2198cb0e0d1b0f27d97085c44c7e8f66d009`  
		Last Modified: Fri, 15 May 2026 20:18:47 GMT  
		Size: 2.3 MB (2314391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a942282ec4ea21b54b037f1f885762bd858b01863a694e6e224128eb9b9362`  
		Last Modified: Fri, 15 May 2026 20:18:53 GMT  
		Size: 226.9 MB (226931022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:bbd0eaa0200386e964e53f4ec9e73f18ad59bce8a0879c8ce0a3148164edf839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2ec6f71e9d7a523138b1da6c28502f5c3633cf6cd533e10f26a717f29e26b6`

```dockerfile
```

-	Layers:
	-	`sha256:933392b1bc7596a3b269c869c3078aa34dc2d6be5e88ecbe9bbbadb5d005fd00`  
		Last Modified: Fri, 15 May 2026 20:18:47 GMT  
		Size: 2.3 MB (2277311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42333c3c840ba2284b4d0ebd38a2929d0c5301b341ccecb2d701a4b616ec032f`  
		Last Modified: Fri, 15 May 2026 20:18:47 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
