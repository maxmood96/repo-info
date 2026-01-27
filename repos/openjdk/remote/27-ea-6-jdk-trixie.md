## `openjdk:27-ea-6-jdk-trixie`

```console
$ docker pull openjdk@sha256:7bc90f6dd63b0bba253ac4690c1811859d023bbdeb0e3fe7d1112611e1168060
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-6-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:e2fea178eb6f99d982b93d5bbaf06a7cdec206565f99826f0fa4bea947805252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.1 MB (387090841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1266a97caed49067c772ffa7f9f35ee6b66ea47e3fd5eb6a2ade055653e44a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 22:11:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:11:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 26 Jan 2026 22:11:49 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:11:49 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:11:49 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:11:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:11:49 GMT
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
	-	`sha256:2bc80a9fab924b134b7244de045828e9c06fa75730e91d20b091f4014ef09d9f`  
		Last Modified: Mon, 26 Jan 2026 22:12:11 GMT  
		Size: 16.1 MB (16062818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6d68d7166e870e2b2837e7921c3ec2858deedae8c8615982c2fa94b7a364fb`  
		Last Modified: Mon, 26 Jan 2026 22:12:16 GMT  
		Size: 228.3 MB (228342216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-6-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:8c08d5cfa5307ad656c9f7eb40a659a7b38e3ac225ec68144d511c511dc0d545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8528906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05453f6a4d351ca3413f986dc785c2089ff6820bcd317c42050c75cfb06a13f0`

```dockerfile
```

-	Layers:
	-	`sha256:7e08706803f83bcbc0cde4747bd9b8f5eecc4f2cb27e41ae33d5bd5ad17e96fd`  
		Last Modified: Mon, 26 Jan 2026 22:12:11 GMT  
		Size: 8.5 MB (8511010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a2839b6b7099e2ab3bdbca637e34bfe23b424eb858e4272bb3df8cca20251e0`  
		Last Modified: Mon, 26 Jan 2026 22:12:10 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-6-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:300b895534021763afd308b196a58e273f6b33a17a4fcaf03bae26614b36d474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.6 MB (384596645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a200597718119770ddae550dd1e031fb9b983f392e086e802223306a6ff683ec`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 26 Jan 2026 22:10:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:10:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 26 Jan 2026 22:10:56 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:10:56 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:10:56 GMT
ENV JAVA_VERSION=27-ea+6
# Mon, 26 Jan 2026 22:10:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='394c8962532cfeb8e27701615449f453f090145d33f7d24947aa6ceed07dcce6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/6/GPL/openjdk-27-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='e516f107cd78b8abf3500494b93d20718e0779fa79a12399f30928c615593789'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:10:56 GMT
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
	-	`sha256:ccf76c401352deb3920b075b7454fb17bb59c3d564b27cf0f4c580ae5d497d4b`  
		Last Modified: Mon, 26 Jan 2026 22:11:22 GMT  
		Size: 16.1 MB (16071508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500281c4585772f84303052b475da0458bcc57ca391dfd52fb8c80f79754d431`  
		Last Modified: Mon, 26 Jan 2026 22:11:27 GMT  
		Size: 226.3 MB (226262905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-6-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:bdbe39487a358a8fcde041c0395ab59f94f435832318d2f4f71d3cad5b3112bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c680c76193dcd1519be5358653f8b42823f16451b9bcd9b15997f1d42f608ea`

```dockerfile
```

-	Layers:
	-	`sha256:e477448eb8e6382653ae0513249e4921f449eb16a10c4d01f1a8e94dff2eb9f2`  
		Last Modified: Mon, 26 Jan 2026 22:11:22 GMT  
		Size: 8.7 MB (8705800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80f9c11ac2f32b5e733200f002a7d515ea6e1827f577cc4dee5ed14aea174060`  
		Last Modified: Mon, 26 Jan 2026 22:11:21 GMT  
		Size: 18.0 KB (18015 bytes)  
		MIME: application/vnd.in-toto+json
