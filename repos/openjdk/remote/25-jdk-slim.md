## `openjdk:25-jdk-slim`

```console
$ docker pull openjdk@sha256:d4065c113470c84a0ba47460a40fe7b5a9c88b18c7a6669b6714cb85aa05888d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:eb75abf82728ae02d9272d000c7dae005319467e4539c3f3707f88418319511b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244657892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c499a0cb456a53e89cfbf62c4757860f5b9a0f8ad0a6e08ab0a3d96deef2da`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Apr 2025 00:48:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 05 Apr 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Apr 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+17
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='00bbc15cf87c83f1fe8dbd30f9ed76caff477401595491d90401b62faf63d82f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='e9a99879baf7d21abe587540977d4c09f8b79ece7a79aacdb9bf8da6c8ce9ff3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca122714a8d7c7287faa7086c69faa956faf2093e47ac466b528f0cfa903990`  
		Last Modified: Tue, 08 Apr 2025 01:27:13 GMT  
		Size: 4.0 MB (4018372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7f27accf3214d3c95b787149af80556dfbf94c2943f44b35d03f865a7a85cc`  
		Last Modified: Tue, 08 Apr 2025 01:27:17 GMT  
		Size: 212.4 MB (212412261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:21e98dedc48d53ce16e707515d2cf5f7af65a0643693af66f7938ac418ff761c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0965d432dfb0e9cc3b6fb47d5b6cc555ef0901bdd8275db8a07a74d819ec0a40`

```dockerfile
```

-	Layers:
	-	`sha256:4c13462e803cb1b5725410bc092824edd50f26193801b61ca44320a5fdac453a`  
		Last Modified: Tue, 08 Apr 2025 01:27:13 GMT  
		Size: 2.5 MB (2535252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4718ad3ff91badfbd7d57d20ee837ca63d75c4e31cfa467177b5aa3320df7eda`  
		Last Modified: Tue, 08 Apr 2025 01:27:13 GMT  
		Size: 19.4 KB (19441 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bfa30e18ac15d938c08ca27de5b59f246b2f908201066c9fdfe9c82cdbbd74e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242114934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386780354e08a5ed42dac2be197aa3e4d137fca199d161f13ad1793fe34f64ae`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 05 Apr 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Apr 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Apr 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+17
# Sat, 05 Apr 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='00bbc15cf87c83f1fe8dbd30f9ed76caff477401595491d90401b62faf63d82f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/17/GPL/openjdk-25-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='e9a99879baf7d21abe587540977d4c09f8b79ece7a79aacdb9bf8da6c8ce9ff3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Apr 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85002c03aaf9b2a8b6da54a3c02fb9e79017b35408eacd8f0e5615650794d7ca`  
		Last Modified: Fri, 21 Mar 2025 17:26:26 GMT  
		Size: 3.8 MB (3833732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84a6dae422e2de1acc3216a7dd71b3778dd0fa05426e1f9cc3e984121128837`  
		Last Modified: Mon, 07 Apr 2025 22:54:31 GMT  
		Size: 210.2 MB (210237165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:fe46a01cfeaab4555d4fcbe526261492991bcbcfe95640028279f9b13fb67e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0cfe5a4112b56220e87ffa364414621a72affe0319a5f04c4a8b7e4864e73d4`

```dockerfile
```

-	Layers:
	-	`sha256:da8087d150defea9fd33ec2d19ece4af33b895c8c1a6c5fc49856fb2dd972c46`  
		Last Modified: Mon, 07 Apr 2025 22:54:27 GMT  
		Size: 2.5 MB (2533680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe83499da33214edea191733821d17d526977094ea38e86f17c70ad9c74e73d8`  
		Last Modified: Mon, 07 Apr 2025 22:54:27 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
