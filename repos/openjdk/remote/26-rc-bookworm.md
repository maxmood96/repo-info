## `openjdk:26-rc-bookworm`

```console
$ docker pull openjdk@sha256:7c5caeab202a8038fd1c6e60028037bec9488403b1d9de629783f303ab1ec4a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:c856463ed6228494d0dc2aeaa0f18cd7b34aba6ded417b492247a39998485d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381922458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c807e698b1eeb91322acf04b60ff9ec9ac0c1b64d31ae2c4ebe979dcfe3636`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:21:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:21:30 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 17 Mar 2026 00:21:30 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 00:21:30 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 00:21:30 GMT
ENV JAVA_VERSION=26
# Tue, 17 Mar 2026 00:21:30 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Mar 2026 00:21:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf051f1897bf7109af670b243c7791c62723fc1ebbfa516af2522da6c8c99a9`  
		Last Modified: Mon, 16 Mar 2026 23:25:05 GMT  
		Size: 64.4 MB (64395521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aded95f9e45f952f3300cd3c229ce68dfb40ba5b8a466e7564c9e729da25c47b`  
		Last Modified: Tue, 17 Mar 2026 00:21:54 GMT  
		Size: 16.9 MB (16945138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b04de911f9d1e51116ca3438d4a6d11888b67427daa08ab5c17d3f6455f58f`  
		Last Modified: Tue, 17 Mar 2026 00:21:58 GMT  
		Size: 228.1 MB (228054911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:127fc5a2c6257d014d4dbe4d01820908d8908f96d24a4af5a14e71c1e0938d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef57e1d6a36e46743c5caa93de1c3aa63a89ad13586bfe6e3023a0cb9aec129`

```dockerfile
```

-	Layers:
	-	`sha256:1676ba79aed3e3d9079f5b985b6035157d230e22e796f8a5c51c11e165b5f776`  
		Last Modified: Tue, 17 Mar 2026 00:21:54 GMT  
		Size: 8.7 MB (8668844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd7496d03b34ef00b4867b41b82b76df696f346d4a1e958b320e1022118afbd`  
		Last Modified: Tue, 17 Mar 2026 00:21:53 GMT  
		Size: 17.4 KB (17351 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:715bd4bdbbc27387c6215a5f9635a9d1a2dc589de9480c28d9c6b37f3224d0a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380166529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4727e6725f9eef948574468be03e0c8f29c4a8ed176dc7a318e684499551e4e1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:19:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 17 Mar 2026 00:19:38 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 00:19:38 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 00:19:38 GMT
ENV JAVA_VERSION=26
# Tue, 17 Mar 2026 00:19:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Mar 2026 00:19:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59add442110ab916af1231a98d110e965b9b107829a3f0920d6789fa955d0`  
		Last Modified: Mon, 16 Mar 2026 23:30:22 GMT  
		Size: 64.5 MB (64479442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5a5631ded03dd79130c3c7874c38fbe7dff2d61b6f14e96d68ce057cad5c9e`  
		Last Modified: Tue, 17 Mar 2026 00:20:04 GMT  
		Size: 17.7 MB (17729035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c84c0ddba4d5ff8714f4025b24c5cfd8fc5a8ddb7218df116ea4903a4be18ad`  
		Last Modified: Tue, 17 Mar 2026 00:20:10 GMT  
		Size: 226.0 MB (225980319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4eb47e3a629e9da7308af0b36b4d39f0dff49d3032b911041683085db1d1bcde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9551ad9e841de3e245c78d03b97f0281f8f8a43d2cebeea7f23a4f64678ecb`

```dockerfile
```

-	Layers:
	-	`sha256:ac610dfd3498da32a43ba2e8989328e01f14912b12123ed5eec163ad622ef445`  
		Last Modified: Tue, 17 Mar 2026 00:20:03 GMT  
		Size: 8.8 MB (8805665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abad65476206cc0ec7400e9452b103ea19924605ec5952883547e0288174e6a1`  
		Last Modified: Tue, 17 Mar 2026 00:20:03 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json
