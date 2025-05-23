## `openjdk:25-bookworm`

```console
$ docker pull openjdk@sha256:6725d32be2c5a8eee82b859a246a61e960f88c61d737bb3ed82efeae5a234f82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:40f54e43eb5c2c1b2ba9b10202569c5618d2e78d2c4d70f8b248829dbc3b250f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367833430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebdb4788dd24d6bec5927f8ac5e3328d020b21eb134f9885f4e2ec6cec13426`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 23 May 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='e47e49dfbb2ad32aa825a587f7aa6829a8ba6fac2b7f60d4cf5f38d8c5241c3e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a4306d6d5c87e8c33dc9a7cffa13b9c984f7173cc4921bce549781c5ada23cd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 May 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8330d934a37ac7b93db00a8a18efe2858aa078c6c0d1cf112d29dd8dc74e216`  
		Last Modified: Fri, 23 May 2025 19:55:25 GMT  
		Size: 16.9 MB (16943386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8633d2a149dd6bd72e6e1d0555ae2a1781baf3b8d63f36b38289e567d66bf6`  
		Last Modified: Fri, 23 May 2025 19:55:30 GMT  
		Size: 214.0 MB (213986306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:398318a28f2ea9f0ebd157b086ceb3c58de484064b7fa92f4f5ab5f174c209ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8486605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a0435e9923e545832a0888906f02598d142d4b6365ba7d741e738cda32cf41`

```dockerfile
```

-	Layers:
	-	`sha256:89c4ebf35ba7047d63fa0471ad1be2f5ff404d62f299ffcf1a18dd86593395d6`  
		Last Modified: Fri, 23 May 2025 19:55:25 GMT  
		Size: 8.5 MB (8467987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:808943e3cca716e19cbc1a00346e0349c3ede0a2e51c67a1fe6210b7b93d67df`  
		Last Modified: Fri, 23 May 2025 19:55:24 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5b3557da721dc5c00bcc6ec30ab8e09dcac22e4d3e363e0fd95540f6c6ac1bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ecddc4fd44c791528daaeabf63d230d15d3b414f9b95e811682a23435dd77d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 23 May 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='e47e49dfbb2ad32aa825a587f7aa6829a8ba6fac2b7f60d4cf5f38d8c5241c3e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a4306d6d5c87e8c33dc9a7cffa13b9c984f7173cc4921bce549781c5ada23cd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 May 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Thu, 22 May 2025 02:47:26 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Thu, 22 May 2025 09:17:58 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de76dec09f06ac58d46e7ad42c61b40fd1d900b4db39da14afb07285ae5aa3b`  
		Last Modified: Thu, 22 May 2025 13:03:08 GMT  
		Size: 17.7 MB (17727125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f513f8178524fb004b7b04ff64165e55204d54750293673a1c1d6459cce33f3`  
		Last Modified: Fri, 23 May 2025 20:06:35 GMT  
		Size: 211.8 MB (211758474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f7fce8824f269a35ebbe5e565c3ea271e09f1b32dc12ab6e0a9b8274a4719df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8623616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6c838e4de97b8b01f27da818c8b82c8302122b6b961223cc47e6e10b8fd2bb`

```dockerfile
```

-	Layers:
	-	`sha256:1508e5aa40aac97a450bb950771af96722acc39be0c80bb71ae542450348e168`  
		Last Modified: Fri, 23 May 2025 20:06:30 GMT  
		Size: 8.6 MB (8604855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dadaa06f107c8196acb69b17f3e75056fd21f513f42b61fcfd5fe9423299d38`  
		Last Modified: Fri, 23 May 2025 20:06:30 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
