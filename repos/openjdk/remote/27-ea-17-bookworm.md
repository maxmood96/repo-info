## `openjdk:27-ea-17-bookworm`

```console
$ docker pull openjdk@sha256:06d5a3fc62b7cd8edc367e9758bd37c8401e5932d07517bc472aa0809da1ef21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-17-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:50c413f77079c715dbedd5cd40f889cb1cabc479aa58d8bba751589630e050b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 MB (382837111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c402058cf70d1975146519c7255f8d45c1181f25da047e07ed88e2090f566f9a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:01:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:01:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 14 Apr 2026 00:01:31 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:01:31 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 00:01:31 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 00:01:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 00:01:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de73ef470b7b271fede6f98a4c8376971bd059ce04ebc13b9f86e34e534b89ae`  
		Last Modified: Tue, 07 Apr 2026 02:43:01 GMT  
		Size: 64.4 MB (64396012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17a16a59f48508d9b5fa1d1c9877779251fc84662abc35fde7bb7a25ce2e544`  
		Last Modified: Tue, 14 Apr 2026 00:01:56 GMT  
		Size: 16.9 MB (16945791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289e9c368eb8410141171a731fec3084a15ce8e5f62db6cd28d0aa42106e014e`  
		Last Modified: Tue, 14 Apr 2026 00:02:00 GMT  
		Size: 229.0 MB (228968216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-17-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:525083a2133ea3852a23ef0a4c8dd14f9d67c0b15998ea73e215911efcd090c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0726232f988d91a94d91f017c0685ef5e857fb3e2ff10a399b49cd069bffcfe7`

```dockerfile
```

-	Layers:
	-	`sha256:e58ad6b624a747ca03c6e8f02f3c20a5c458df8e8cb1a0cfbfdb9f403207c083`  
		Last Modified: Tue, 14 Apr 2026 00:01:55 GMT  
		Size: 8.7 MB (8668887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57e90719e658d6fde41f86846af14bf4667e42bc31bd8b599adbaabc9c8d35e`  
		Last Modified: Tue, 14 Apr 2026 00:01:55 GMT  
		Size: 17.9 KB (17937 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d14f690d9fb80b133528741d940b43ecc65f2a19161b6d6d6f2ce04f31e6214c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381113617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b773e21102d6ae51d9e9a7e50af05158e860dc9557a0450697c7417a23770c7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:52:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:02:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Apr 2026 00:02:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 14 Apr 2026 00:02:48 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:02:48 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 00:02:48 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 00:02:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 00:02:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b913dee6e116304b9bb2391ef8aedbb1f5ee16d167338920c7609a48bdd772`  
		Last Modified: Tue, 07 Apr 2026 02:53:06 GMT  
		Size: 64.5 MB (64479508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad5efe4a49fb5ec93788750563409b633160986b78a1d45fa103f7a4541110`  
		Last Modified: Tue, 14 Apr 2026 00:03:16 GMT  
		Size: 17.7 MB (17729119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f5bb7e23494928e276fd28aa57bc89f118dea5c8d2d8faf4dc2f5d49744e37`  
		Last Modified: Tue, 14 Apr 2026 00:03:20 GMT  
		Size: 226.9 MB (226927023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-17-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:1db00f8f773786881e54cae0ceb1c98777baf00294dd8c6404b5df2fc0281081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f96a2e2db72de6da84d51a16a442dc94c5b5a9c12d0483b28db55df876af389`

```dockerfile
```

-	Layers:
	-	`sha256:bcdcba31a67f9f81f6248659dd991e3b897a1ae3bb5f5a35fd156c6bc09c6b6b`  
		Last Modified: Tue, 14 Apr 2026 00:03:15 GMT  
		Size: 8.8 MB (8805732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a347d81d61dca17f4d7fae587d8e60f9947fd747de138bc4016c53dd6665f66`  
		Last Modified: Tue, 14 Apr 2026 00:03:15 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
