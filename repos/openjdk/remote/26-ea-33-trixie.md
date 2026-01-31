## `openjdk:26-ea-33-trixie`

```console
$ docker pull openjdk@sha256:d74b5d0a9236dee1feb43d06bf53ff4248f41eb15f3f4df55a9adab1b9fdb504
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-33-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:e157788ee16147a87949fef4080beae1bcee75d102e07ae1eef2f8c266bc6d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.7 MB (386737937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e17f15d6065d09bcb5c146e33a2f4debed66cfbfe909a0e260f434fafea4f5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 30 Jan 2026 23:40:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 30 Jan 2026 23:40:23 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:23 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:23 GMT
ENV JAVA_VERSION=26-ea+33
# Fri, 30 Jan 2026 23:40:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:12 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:29 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cf0a97315574d3ab1d6a3c224a27bc2d61ad06bbb323fcaf4704c849d596a9`  
		Last Modified: Fri, 30 Jan 2026 23:40:47 GMT  
		Size: 16.1 MB (16062881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed9ca2bb31a1bc22fb917d8d7bbd5564d496fb03b1f073b2d7efac33412402`  
		Last Modified: Fri, 30 Jan 2026 23:40:51 GMT  
		Size: 228.0 MB (227989249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:86be0aa6bb7406ee152d3526ae67c0616bb7d9ffd5d8ad153d856a025e969f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8528931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b563592b1691d141a4e4caa127a2790fedd18ef7078e5b5f406b18fcbc58cc44`

```dockerfile
```

-	Layers:
	-	`sha256:4a7d20533b9c03f7159e0956381463d302683adeeaac3d82f93200e438080282`  
		Last Modified: Fri, 30 Jan 2026 23:40:46 GMT  
		Size: 8.5 MB (8511018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d89503a0ed812c787c6486f4d66d6a618b106805e7f13bdb260f255a57641f20`  
		Last Modified: Fri, 30 Jan 2026 23:40:46 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-33-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e757963e712d862593daad7151547d18fb70c9ae4325c67c91874fb320a12732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384236657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2889718ff6023f94d89db340eb597122b8eab958d642b264e13c38e41126fe`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 30 Jan 2026 23:39:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 30 Jan 2026 23:40:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:13 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:13 GMT
ENV JAVA_VERSION=26-ea+33
# Fri, 30 Jan 2026 23:40:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:36 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:39 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483b756101326cc34d17b6bb29174847e6f15238d4bbaabd9609896322d9623c`  
		Last Modified: Fri, 30 Jan 2026 23:40:39 GMT  
		Size: 16.1 MB (16071557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f5a3346067cf1e1647ce00a597dd903810a105ec4a6994da1eb18c75b2e292`  
		Last Modified: Fri, 30 Jan 2026 23:40:43 GMT  
		Size: 225.9 MB (225902868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:a2c8b9c5e052d770cfb786ce053979e3b50e7e6525d391476d4173d4ed1bc9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bba85e7c3de136977a16eb178402322cff4a1840caf616d10e93d352a904e55`

```dockerfile
```

-	Layers:
	-	`sha256:a722da539ae3758be1754c0f7512ddd8b696463e3305aafe3abb912bf57e8fcd`  
		Last Modified: Fri, 30 Jan 2026 23:40:39 GMT  
		Size: 8.7 MB (8705808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0b03911f37c084d3835c055c3f8dad1ea9f8e6a7123f49390d85db4ea071c21`  
		Last Modified: Fri, 30 Jan 2026 23:40:38 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
