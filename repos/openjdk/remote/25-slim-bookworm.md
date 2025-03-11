## `openjdk:25-slim-bookworm`

```console
$ docker pull openjdk@sha256:f85a7e6b4ba6ee6af52530f3ff92d2e8ea603b8c5a4705e70c3fb347e3eaa3c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:76e2a10de315a5ab3d7c8fd107ac004d7b98553b9140c39300b4fa60ae0de3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244058441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d8bf6d7f1ace6e3dcc959894990864ea2c47de7bb550063cb1ea3415bc72fe`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 08 Mar 2025 01:48:16 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 01:48:16 GMT
ENV LANG=C.UTF-8
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_VERSION=25-ea+13
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='456a1dced4795cf35e28459b6289a9eb1d6921f83c79cf460c5c694cb52e11ba'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='518a0d1c64c68f4563c167e052f135827c1b218933dd68a481a7973694fc64b2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59470e789f9f9aa24f3aec421020aa27a5306b37ab3f18dd85b8d3754aa5115b`  
		Last Modified: Mon, 10 Mar 2025 21:05:59 GMT  
		Size: 4.0 MB (4018432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbca7cc389db7669eae61879fcafab6fa157c08dcf29e3445302b23b219694f1`  
		Last Modified: Mon, 10 Mar 2025 21:06:02 GMT  
		Size: 211.8 MB (211820708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d22268895a8ab4aa50cf18721d085a3dfcc53da6b0ab0d2e266fe776d82a603d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16377c4471af92d9bc41b218214188eace6a2668414eb22ba876902013c33269`

```dockerfile
```

-	Layers:
	-	`sha256:8bed69d6540da876ed73fb92dd33dc0f4d02d9abcce72e7285f4080e0c0ff4cc`  
		Last Modified: Mon, 10 Mar 2025 21:05:59 GMT  
		Size: 2.5 MB (2533908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dedd7bd47fa891f2b2c7af74801e7ae5b3ca0db941eb503ca4550865a49a9e38`  
		Last Modified: Mon, 10 Mar 2025 21:05:59 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8b8280464f510aee3bbb64d070acc6efeb1a1007285f1c9f777d2eef8c05e37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241641578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14788ccabe974410851f6d204dcb87c3041cfa98de604b35d54e779186c4cf27`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 08 Mar 2025 01:48:16 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 01:48:16 GMT
ENV LANG=C.UTF-8
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_VERSION=25-ea+13
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='456a1dced4795cf35e28459b6289a9eb1d6921f83c79cf460c5c694cb52e11ba'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='518a0d1c64c68f4563c167e052f135827c1b218933dd68a481a7973694fc64b2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24b764fefcf12f640abdda9274a0cb11d639b180f003a673e0766704dec6540`  
		Last Modified: Tue, 04 Mar 2025 22:00:24 GMT  
		Size: 3.8 MB (3833778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3613f39094f4c48f20c9294f7658d5e4c48a6fafb12e6e19c67f1980adf0aca1`  
		Last Modified: Mon, 10 Mar 2025 21:57:34 GMT  
		Size: 209.8 MB (209759375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:65fa129e3b89bd00cbaa9dbf7ccb81140c398ad5c032bf07159649d8c20c0cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a738cad920b1e3b5ced59dca3aebcbaac53750e8b333a5bcf99d7f7dbe3589`

```dockerfile
```

-	Layers:
	-	`sha256:693da31d25560695ff3f22a2dc3711531532e0405b9b679d35cf1df4bfc33ab8`  
		Last Modified: Mon, 10 Mar 2025 21:57:29 GMT  
		Size: 2.5 MB (2533638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7244001215ccf4904d606e7f44eb34bc7305963a445a63fcffdc5d75d29baa15`  
		Last Modified: Mon, 10 Mar 2025 21:57:29 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
