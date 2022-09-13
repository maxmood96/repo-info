## `openjdk:20-bullseye`

```console
$ docker pull openjdk@sha256:cb4355ce0abd959c0eec90f599bab8bf24443cb428e3a228a5ea3846bdf6ad52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:dba9fa50b885f43c9b93d67d62a3d7e1c48f6c9e243bad8620008d91b9c77ac0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336655540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2fa6648d362eacd9cd11e4dfd73a330e9bd27e668e18b4bfcde1a6e0b3a9c8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:40 GMT
ADD file:6944d322f4c04bd2192061822af5cbec8ac0a6b424c461d66174d32aed604972 in / 
# Tue, 23 Aug 2022 00:20:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 00:48:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 23 Aug 2022 00:48:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:29:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:29:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 23 Aug 2022 04:29:11 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Aug 2022 04:29:11 GMT
ENV LANG=C.UTF-8
# Mon, 12 Sep 2022 22:36:17 GMT
ENV JAVA_VERSION=20-ea+14
# Mon, 12 Sep 2022 22:36:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='ce9c99a0d70bf7c6548b68a33770a50d1273d5d5ea72522a1fe91ae6d3f22c1d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='4935236eb4e51be13ddfcc1ce717191128feb8ff9329676971ea54775261d9ff'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Sep 2022 22:36:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1671565cc8df8c365c9b661d3fbc164e73d01f1b0430c6179588428f99a9da2e`  
		Last Modified: Tue, 23 Aug 2022 00:24:32 GMT  
		Size: 55.0 MB (55007555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e94d13e55e7a4ef17ff21376f57fb95c7e1706931f8704aa99260968d81f6e4`  
		Last Modified: Tue, 23 Aug 2022 00:55:37 GMT  
		Size: 5.2 MB (5163019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c7528c685216129e8e67bf362a7702e7b1daa585ab85546a41508830657d6`  
		Last Modified: Tue, 23 Aug 2022 00:55:38 GMT  
		Size: 10.9 MB (10876472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ad072f9cd16fc8eb93b182b20e758e11acc0ef60babef0bf1043c08de1901a`  
		Last Modified: Tue, 23 Aug 2022 00:55:57 GMT  
		Size: 54.6 MB (54584135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceff553f4bee69a32b1ccc5ae9b10a5658314786894f7eb732f5870a77168241`  
		Last Modified: Tue, 23 Aug 2022 04:35:56 GMT  
		Size: 14.1 MB (14071889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bf4b70996a8d78c082423db6b144463bb649cbb1f4496e2eae820e77d940b7`  
		Last Modified: Mon, 12 Sep 2022 22:42:01 GMT  
		Size: 197.0 MB (196952470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:76e893c3311148a4186ee67e9030a42f9c47900e051675f77e2af4673fa4516c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.0 MB (334971002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff7405fd5e4d15824fb5fae1051e15c8dea26a1ac98c54bc0c54141a98e5d21`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:16 GMT
ADD file:ce6014a27d18915dc6d46c5c1f0f894f0027d1e41fbebb1599c16371b7bab2f1 in / 
# Tue, 23 Aug 2022 01:52:18 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:28:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 23 Aug 2022 02:28:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 05:15:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 05:15:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 23 Aug 2022 05:15:30 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Aug 2022 05:15:31 GMT
ENV LANG=C.UTF-8
# Mon, 12 Sep 2022 23:04:50 GMT
ENV JAVA_VERSION=20-ea+14
# Mon, 12 Sep 2022 23:05:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='ce9c99a0d70bf7c6548b68a33770a50d1273d5d5ea72522a1fe91ae6d3f22c1d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='4935236eb4e51be13ddfcc1ce717191128feb8ff9329676971ea54775261d9ff'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Sep 2022 23:05:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd84405c8b9e7a8c3d580c2148d25120dd697ea61e1cb55a62f33e67988b7043`  
		Last Modified: Tue, 23 Aug 2022 01:57:29 GMT  
		Size: 53.7 MB (53690830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d98e120b809269e56de468d2b91569789c521011e4d9b1806e43fd04462de2`  
		Last Modified: Tue, 23 Aug 2022 02:36:44 GMT  
		Size: 4.9 MB (4944180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb6be5911b40ca548e48c10b09cb2312f1698b4c84f09711c69389a94b1a8be`  
		Last Modified: Tue, 23 Aug 2022 02:36:44 GMT  
		Size: 10.7 MB (10657442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db608c3c3ce3568556faf63acbc2069811afe242faf8992ccf0ab1986ee38e4f`  
		Last Modified: Tue, 23 Aug 2022 02:37:07 GMT  
		Size: 54.7 MB (54680886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb21073e82e2e0d1f250d23308b347ef16d5f0c291dae4ac50949650ba5aef0`  
		Last Modified: Tue, 23 Aug 2022 05:26:59 GMT  
		Size: 15.5 MB (15527194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b35d1e63a82082149659aa630b6dd9c20afe45a9aa31222c2b4b4daa87cdde1`  
		Last Modified: Mon, 12 Sep 2022 23:14:35 GMT  
		Size: 195.5 MB (195470470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
