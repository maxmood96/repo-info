## `openjdk:26-ea-jdk-trixie`

```console
$ docker pull openjdk@sha256:10088f5cc3b690a421498e79ab4210ee6f1670f03bbc5602f8fbd974a6cac852
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:32d0d81d763d3ea76ca5dc23811826b6adf1144383bad532dcbeed93fdf42277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.7 MB (384702187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1407661ecc57c6a0ce3ae19aa3e7bf3d2673eabb36b49a3e32eccc062543fbef`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:42:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 10 Nov 2025 19:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:53:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 10 Nov 2025 19:53:01 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:53:01 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 19:53:01 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:53:01 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='c5cb587a920ddf65225352cf2494965786acd1de8d6748a976d7498d0783a396'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='427f53a6635347b853f695324253b6d78f69cc09334a9cb1031a801e43358883'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 10 Nov 2025 19:53:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3143549f2b8b3ad8d79efdc47824641c6771796b3770f3c637a38aabd2b3462`  
		Last Modified: Tue, 04 Nov 2025 04:14:53 GMT  
		Size: 25.6 MB (25615393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e8e93b0d018b135d833207c6feaba205653ac52e0a80d214477ec0de239dee`  
		Last Modified: Tue, 04 Nov 2025 07:43:02 GMT  
		Size: 67.8 MB (67776858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e070463136186b5daf1e4038ab867a507a2f75e6c75dfdf36636f4102c19fa`  
		Last Modified: Mon, 10 Nov 2025 19:53:44 GMT  
		Size: 16.1 MB (16061453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7781e9987dd1b84ec6e15eb3c7ab7951b599268199abec96242cc4b672b3b5`  
		Last Modified: Mon, 10 Nov 2025 22:29:07 GMT  
		Size: 226.0 MB (225962855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:9253b601ec9aa32b6404421be94c6d6f6f30352a760f19b9fd29be91dd3703c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc1e7bfa1e30057ca12f53dcb86f8576e5bb56a21a49bda267498aecedf2a33`

```dockerfile
```

-	Layers:
	-	`sha256:5b2238f7f211c72ba9ca437fea3a56a7b17cdaf5877fc19097efecde29dd7983`  
		Last Modified: Mon, 10 Nov 2025 22:24:25 GMT  
		Size: 8.5 MB (8509895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dca0dd7c27c722e926ee599ad91058addca6eab9441b93e559c5a42f0ec5dd8`  
		Last Modified: Mon, 10 Nov 2025 22:24:26 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:002658181030174c0b74efa2bfc50f6f29cf3b11d72dc177789fe354f851050d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 MB (384015283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d77df595ad28677154c3efb61ebc46f64be7cf2e82d3d0f1cf591bd03983f31`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:43:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:43:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 18 Nov 2025 06:43:12 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:43:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:43:12 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 06:43:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='4ba2cf8ca6a66fbea892ba55048f82d8cd4fabe95d9364ac28a79b282c6207f8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6f947b5c9fa605b41f4890ef6e09f2c0c321215681497f2174efa10adfab326'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 18 Nov 2025 06:43:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a65cbde52b7a9f6f7d2f56f40b187864703af947ffc00445be4ec354d186c6`  
		Last Modified: Tue, 18 Nov 2025 06:43:48 GMT  
		Size: 16.1 MB (16070645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8db234f6cdac2b3582ab0f7e66ae39a47fa60d012299ec5ec570227f651a23e`  
		Last Modified: Tue, 18 Nov 2025 08:15:44 GMT  
		Size: 225.7 MB (225688633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:008c68daf64ff0a29b449c67f81108344b534e823cc23ec3b7549fd8fccabd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca70d527f82d15df94111989764ab2e5b82a508ad2765ac5cde301bb1f9db02c`

```dockerfile
```

-	Layers:
	-	`sha256:0203e421b96a34793794f51a3a49d358996d704fbfe4abcdb0bf12f68bca2135`  
		Last Modified: Tue, 18 Nov 2025 07:25:20 GMT  
		Size: 8.7 MB (8704733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66357dcda0d5ff0778a572dbc278f73df5eec4557ddb72ff3dd75b4f35d6c0`  
		Last Modified: Tue, 18 Nov 2025 07:25:21 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
