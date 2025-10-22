## `openjdk:26-ea-20-trixie`

```console
$ docker pull openjdk@sha256:4fca49dda51d77c48616d764609f6205d52e54310cfdf11f305842f91c21fb32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-20-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:786ad3afca825d2c2afdc6198fedd400072b1e07ace529a32ebf3c18fb9231bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384537522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1450150b7adc291021cd31a38858d17f1c19a9d2f075dadd5aa699a575c6c9e5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 20 Oct 2025 18:48:18 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 18:48:18 GMT
ENV LANG=C.UTF-8
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_VERSION=26-ea+20
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='5a59bcbbbee3ef3870abde737d101b8688ff06144c853ff29ef6ac8247c96a87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='bf2a13c36da561391ccbda5d5d8dcce3963d35f2d5b0819a1fa725999f090aa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d573bf42b377ce6a5a0451c15388849686fa4058efd68999f3b014daeb5b55`  
		Last Modified: Tue, 21 Oct 2025 01:42:47 GMT  
		Size: 25.6 MB (25615545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dfe2fac1c486e9aaf41d1028ed30be2c442aa84af44462bc7bac8c148ffb13`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 67.8 MB (67784857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6952eab25d23e2ee8b590531a1fe2859cfbffd3705be2cbdda978a4ed8deac93`  
		Last Modified: Tue, 21 Oct 2025 20:20:41 GMT  
		Size: 16.1 MB (16061377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c798bf40c83dbc5929e403a5737a5fcc6198d531829773b5c8872c5eaabeb9`  
		Last Modified: Tue, 21 Oct 2025 21:42:45 GMT  
		Size: 225.8 MB (225790772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-20-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d10bcd9d7f7d34aafcd57f8a2ec2f67f7dfa57ed9d853cf1e23edad7b71b1c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8530361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8b915edcf1210bfa4fe7205dc46a7aa871eb36d844f127e3ec16ea58ad4c64`

```dockerfile
```

-	Layers:
	-	`sha256:30ec9410cf86a31d12dbf3aa52490549926325a2607ae8e84ad6e9373f8f3ce5`  
		Last Modified: Tue, 21 Oct 2025 21:24:29 GMT  
		Size: 8.5 MB (8511777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:679879bc30d992f2aab531d1a8ca258701af7cd96f26d469fe905dfd561a80dc`  
		Last Modified: Tue, 21 Oct 2025 21:24:30 GMT  
		Size: 18.6 KB (18584 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-20-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dd7e0c4d8f150ec5bfc976522ee7b3cca9b88991a2fd4d7c2b7beed495115283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.0 MB (381967474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a70cbd30780cd33195abb53d3ea8c305494b8ae93582c67fed8bcc947c039bd`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 20 Oct 2025 18:48:18 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 18:48:18 GMT
ENV LANG=C.UTF-8
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_VERSION=26-ea+20
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='5a59bcbbbee3ef3870abde737d101b8688ff06144c853ff29ef6ac8247c96a87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='bf2a13c36da561391ccbda5d5d8dcce3963d35f2d5b0819a1fa725999f090aa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d4a5d5e5dc9fcf4600bc2ea89f89bb2c7f92855fb486edd7a8c2b002737a84`  
		Last Modified: Tue, 21 Oct 2025 18:13:56 GMT  
		Size: 16.1 MB (16070417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8346743b13fb0c6e776bd29c6757f75a5ef41d48682aa150ba0aa86768c164`  
		Last Modified: Tue, 21 Oct 2025 21:41:49 GMT  
		Size: 223.6 MB (223646742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-20-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:32b59e0de86520750610d278bd8298c43275ce98350622ab6c32372559f2440a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8725318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2813a3d53cb44267f479142307eb0745ab124cd5ebaec6f8027ef0077af3fe90`

```dockerfile
```

-	Layers:
	-	`sha256:8d13113ac16256d6515c3a8ea8ef633fcc5ca0dbe7b4934b22944444e1eabee8`  
		Last Modified: Tue, 21 Oct 2025 21:24:38 GMT  
		Size: 8.7 MB (8706591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:546131ebde35c8dde7f4c5b825a04165ec5e0dfedad736c7e69fe045b8423121`  
		Last Modified: Tue, 21 Oct 2025 21:24:39 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.in-toto+json
