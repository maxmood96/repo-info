## `openjdk:28-ea-trixie`

```console
$ docker pull openjdk@sha256:8bad8e265f394ba62cfeeacda1c7c8f93bc3d93fe43bff40247162e35377afee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:488c0a89435e6187fd3a8b9a17b788a3f540854b6e13cd5b2ea7f2dcf2420254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385933053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985380e244a18f86decbb479f8fc477ab9c17be27343a167bdcb82b39ff52932`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 10 Jun 2026 20:16:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jun 2026 20:16:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Wed, 10 Jun 2026 20:16:38 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:16:38 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:38 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:16:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 10 Jun 2026 20:16:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9dfe264b62e3d63906376b1d59a0352115c11480a4bfe43b7a80c3da6cc262`  
		Last Modified: Wed, 10 Jun 2026 20:17:02 GMT  
		Size: 16.1 MB (16065769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bc370603586f69a2e9adba7ad768d36bf44555072b45d40290e3f83748ee2d`  
		Last Modified: Wed, 10 Jun 2026 20:17:07 GMT  
		Size: 227.1 MB (227145014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:36d054b409ca76c75c3d994267f24ec9f3e70eba3e13648751a8930fea259435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8526671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5aa1cb7180999df145ab72c41b48f9130e54a9b83398b6f316f8a99b9276a64`

```dockerfile
```

-	Layers:
	-	`sha256:ed6daa62b511b72af9f63cdbc29f4d335c7e051c15d09eaeeabb455f4530f39f`  
		Last Modified: Wed, 10 Jun 2026 20:17:01 GMT  
		Size: 8.5 MB (8508775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:673e6ee815034c0aee7f1fb8e8a6828fc9c1f02f2cdeee13d9dbe96a8f81b3aa`  
		Last Modified: Wed, 10 Jun 2026 20:17:01 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:db4a21780439584d22d7b11f6369b2ba44be5fab02d82690e310cc1bbe37049a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.5 MB (383476315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7016fc84143ac5c1d3248d2f4b6f1822e451997b9d945937d4afb9257b92fec1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 10 Jun 2026 20:16:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jun 2026 20:16:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Wed, 10 Jun 2026 20:16:21 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:16:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:21 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:16:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 10 Jun 2026 20:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590f07c9ed877bbf03cd41a51562362447281ff38d87ccf6bd1b790589f6e67d`  
		Last Modified: Wed, 10 Jun 2026 20:16:47 GMT  
		Size: 16.1 MB (16071454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aea04e8a7e8660b4d2044ac942d887d6cdba3b02b301766999e4185a50759e4`  
		Last Modified: Wed, 10 Jun 2026 20:16:53 GMT  
		Size: 225.1 MB (225114186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:bebe914001e9cc173391a4398c823f1155e48808ef6b6548d86523e677dd6d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8720943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac84cd84cb0a65aa87ccfcd1eb258e41e73ecb312772c1603a6d7392d9b79e7`

```dockerfile
```

-	Layers:
	-	`sha256:796822cdccb4c3fa7883ed0c8fbdd150897379fa961ef4762119f7ca53f452cc`  
		Last Modified: Wed, 10 Jun 2026 20:16:47 GMT  
		Size: 8.7 MB (8702928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c852769fae40165ce64146b890ff8185e5d40e180b5417d9a83e4acad6c5fd1`  
		Last Modified: Wed, 10 Jun 2026 20:16:46 GMT  
		Size: 18.0 KB (18015 bytes)  
		MIME: application/vnd.in-toto+json
