## `openjdk:21-ea-2-slim-bullseye`

```console
$ docker pull openjdk@sha256:99dc50a0ec8dabce8beaa9f9f41a8794f3ba59753539826e69f2111ae757783d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-2-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:c9787e19be3c71ea1c3b519fb444a6c7d9cd3b7daf6a3fbda0855f8884239cc4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232346179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca29a0ba22a63984b1d08f650897cda1a5a6051cf643d9a33e6d47f143115075`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 05:06:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Dec 2022 00:33:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 14 Dec 2022 00:33:42 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2022 00:33:42 GMT
ENV LANG=C.UTF-8
# Fri, 16 Dec 2022 23:30:32 GMT
ENV JAVA_VERSION=21-ea+2
# Fri, 16 Dec 2022 23:30:46 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/2/GPL/openjdk-21-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='8070902e5bfbb71a4e7c723bb0439faeb9f3127e1fb048f7ed4e6a5abc5a3505'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/2/GPL/openjdk-21-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='011358a514a8d4030c36bbd5b7d7fb5c404f326498f4c832ee5f890fff8709db'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 16 Dec 2022 23:30:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca06928f532b9db5daaeea1a6cfedc2be5faa3421714209b828baa3f96741b02`  
		Last Modified: Tue, 06 Dec 2022 05:11:13 GMT  
		Size: 1.6 MB (1584014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18caeb72093ead04e3dab587dd38ef45a552d0cffb80bf6eb2df698b9fe2f66`  
		Last Modified: Fri, 16 Dec 2022 23:38:27 GMT  
		Size: 199.3 MB (199349313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-2-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bfea248f4b68f614940529d7171ac24f0651ecebd319b566f89e4a5a6f48941c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229469589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a25c7cfacf7b6b6d900481a4165d76560ddef6b78928cec9e09055987f69fa`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 03:53:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:53:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 21 Dec 2022 03:53:33 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 03:53:33 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 03:53:33 GMT
ENV JAVA_VERSION=21-ea+2
# Wed, 21 Dec 2022 03:53:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/2/GPL/openjdk-21-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='8070902e5bfbb71a4e7c723bb0439faeb9f3127e1fb048f7ed4e6a5abc5a3505'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/2/GPL/openjdk-21-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='011358a514a8d4030c36bbd5b7d7fb5c404f326498f4c832ee5f890fff8709db'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 21 Dec 2022 03:53:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d25ec39ac4d8c95008c4cae68bf15b8d0f09df7a1b2b0b0c892724ec59abbd2`  
		Last Modified: Wed, 21 Dec 2022 04:00:05 GMT  
		Size: 1.6 MB (1566279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b042b137adf63577173834fa78758aafea48c11b16910e664659835589d772`  
		Last Modified: Wed, 21 Dec 2022 04:00:14 GMT  
		Size: 197.9 MB (197858538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
