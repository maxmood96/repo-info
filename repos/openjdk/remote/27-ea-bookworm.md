## `openjdk:27-ea-bookworm`

```console
$ docker pull openjdk@sha256:52b6f49c234460ee5fd7f58d91e443002948fd1ef7637ea294c5925fab01efd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:029b361da9633bdc21cdb36162851f5815f41c81248c5c68a145b0ae11bc119f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.6 MB (382628862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08c0ff76032a58735904c029ccc67955834cb0cb26ac82aa95fbb8fb36db6d6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:50:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:50:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 11 May 2026 23:50:35 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:50:35 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 23:50:35 GMT
ENV JAVA_VERSION=27-ea+21
# Mon, 11 May 2026 23:50:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 11 May 2026 23:50:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0869e5c4dac5849d3555a38db741288a16528478145da8dcb95b8dba2464d55d`  
		Last Modified: Fri, 08 May 2026 20:26:25 GMT  
		Size: 64.4 MB (64397036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94abb0ed8cb5decdc0cb393e070b45e2b5f91998c335459b3898c46979bacb54`  
		Last Modified: Mon, 11 May 2026 23:50:58 GMT  
		Size: 16.9 MB (16946688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6499023eb5785e29917f45f3f7e881a6f5ba37097863720422be6dc03870b18c`  
		Last Modified: Mon, 11 May 2026 23:51:02 GMT  
		Size: 228.8 MB (228754282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:7fc781159c418b833277345c943519ccaf7acd843e55c97db16dc4969c4cd66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8685556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:360ac9e922b5c69387e1524f02bdab46606ca862087d55aa75be9ee931d23df1`

```dockerfile
```

-	Layers:
	-	`sha256:24cf9bba480b19b8e4bb2ff3f46ecfff7d7169b6207e12bcd461c91af972f0ce`  
		Last Modified: Mon, 11 May 2026 23:50:58 GMT  
		Size: 8.7 MB (8667617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2582deffad4a662b23c0dce71658567d8be66acc3246524275b6913a13eb5cbf`  
		Last Modified: Mon, 11 May 2026 23:50:57 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e24ddec658851f63ff446e68aac9502b8ce694722bd54ffc760a2bfc3f4a057e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.9 MB (380914641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a3675cda971a866cac75bfec70a8dfd4399e784dab265bac7b1d6e572d5a51`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:51:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:51:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 11 May 2026 23:51:32 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:51:32 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 23:51:32 GMT
ENV JAVA_VERSION=27-ea+21
# Mon, 11 May 2026 23:51:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 11 May 2026 23:51:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5c3bf1fab727b805a2f735f33789c10938680bdeb2f8922a44aa2738df91f`  
		Last Modified: Fri, 08 May 2026 20:32:11 GMT  
		Size: 64.5 MB (64479741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28af18d6ca88dfa4abcd6349586f8e4e26cffbdea3c6585faea80ee5f0336945`  
		Last Modified: Mon, 11 May 2026 23:51:58 GMT  
		Size: 17.7 MB (17730460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d49cd046aa2acdb9659be630ebd5e8553b753692cc561e81464e344c0b133a`  
		Last Modified: Mon, 11 May 2026 23:52:02 GMT  
		Size: 226.7 MB (226721933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a78c505e597125efcad903839d5f4875c37adb7054e9b4cb5fa618cf4350b684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8822520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1476518cba9ef13400c18f2af44506996ed14a83a942f184b22470e1e2c940`

```dockerfile
```

-	Layers:
	-	`sha256:91d158d2c6dec5733a600a9cdeefc6e19b8f27e64cb53f378a19f0ea73ae9df1`  
		Last Modified: Mon, 11 May 2026 23:51:58 GMT  
		Size: 8.8 MB (8804462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97104ee02c76599637d7bf9029160e1e1d8f853d369922c81d28e95847c9a758`  
		Last Modified: Mon, 11 May 2026 23:51:57 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
