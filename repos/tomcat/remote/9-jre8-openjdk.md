## `tomcat:9-jre8-openjdk`

```console
$ docker pull tomcat@sha256:2c9c32e2a82671c6d65eb3a21918a2f2a3ce0296ae99692030a446ffc902f61d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jre8-openjdk` - linux; amd64

```console
$ docker pull tomcat@sha256:186bf8def179416b62dab9c766104a9810966117c4b3884d1f1827f5632d0f0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130587883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542c63f67179800e17ae46b6206c5b636cd95d2f041d873405dea1cd6e89c6eb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:30 GMT
ADD file:aea313ae50ce6474a3df142b34d4dcba4e7e0186ea6fe55389cb2ea903b9ebbb in / 
# Tue, 12 Oct 2021 01:20:30 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:42:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 16:34:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:36:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Oct 2021 16:36:57 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Oct 2021 16:36:58 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 16:36:58 GMT
ENV LANG=C.UTF-8
# Thu, 21 Oct 2021 23:47:52 GMT
ENV JAVA_VERSION=8u312
# Thu, 21 Oct 2021 23:47:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 22 Oct 2021 00:27:11 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 22 Oct 2021 00:27:11 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Oct 2021 00:27:11 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 22 Oct 2021 00:27:12 GMT
WORKDIR /usr/local/tomcat
# Fri, 22 Oct 2021 00:27:12 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 22 Oct 2021 00:27:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 22 Oct 2021 00:37:43 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 22 Oct 2021 00:37:43 GMT
ENV TOMCAT_MAJOR=9
# Tue, 16 Nov 2021 00:33:01 GMT
ENV TOMCAT_VERSION=9.0.55
# Tue, 16 Nov 2021 00:33:01 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Tue, 16 Nov 2021 00:33:02 GMT
COPY dir:733e1f81da4202a409aade463e1e98a14baca90ab3716fd4bac0a8b245ac1bdb in /usr/local/tomcat 
# Tue, 16 Nov 2021 00:33:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Nov 2021 00:33:08 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 16 Nov 2021 00:33:08 GMT
EXPOSE 8080
# Tue, 16 Nov 2021 00:33:08 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bb7d5a84853b217ac05783963f12b034243070c1c9c8d2e60ada47444f3cce04`  
		Last Modified: Tue, 12 Oct 2021 01:25:37 GMT  
		Size: 54.9 MB (54917520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02b617c6a8c415a175f44d7e2c5d3b521059f2a6112c5f022e005a44a759f2d`  
		Last Modified: Tue, 12 Oct 2021 15:52:48 GMT  
		Size: 5.2 MB (5153273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32e17419b7ee61bbd89c2f0d2833a99cf45e594257d15cb567e4cf7771ce34a`  
		Last Modified: Tue, 12 Oct 2021 15:52:48 GMT  
		Size: 10.9 MB (10871935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab18cfab55f9b2e1184b3f5b90de6574c96bdf1c4c782f4e1879437c38541af9`  
		Last Modified: Tue, 12 Oct 2021 16:53:01 GMT  
		Size: 5.7 MB (5653928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793716e93ecb3dc756176dea4353c0fd34b83be7fe04582df89283781c0e2bdf`  
		Last Modified: Tue, 12 Oct 2021 16:56:18 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9b14f7678b3f0af9568b4869f0100eb02cc4d107d2436284db725c0aabda65`  
		Last Modified: Fri, 22 Oct 2021 00:05:00 GMT  
		Size: 41.4 MB (41372080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2d594b57d6413d65c1791a79189febcd379064f219e565e68f60d82b68bbf`  
		Last Modified: Fri, 22 Oct 2021 01:13:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742a2709a10941557076f28828b0b0e327f99d5dca4456417d2e6b6712c29255`  
		Last Modified: Tue, 16 Nov 2021 00:55:32 GMT  
		Size: 12.2 MB (12159041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c866a468520690ea6a0599df063d51b3df47b8141b04e0c6dcbb882087c46e4f`  
		Last Modified: Tue, 16 Nov 2021 00:55:31 GMT  
		Size: 459.6 KB (459593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331bb8edd8a6cc9268ff733db78d75eaa75bd6ec3a4f74912a67f78c7cbec7c6`  
		Last Modified: Tue, 16 Nov 2021 00:55:31 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-openjdk` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:1c905da0944a0eb8575a9061e3ad9883334521a5fa9abb4d235cf9778b484642
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127869967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2997428f220406d7fc7cad724b960d6db4ff9c6d89a5afc435433c925163053b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 17 Nov 2021 02:39:59 GMT
ADD file:eb667e18226da8a1ca5a41beacddc65cd1efec01c3d01e50845c5e89e91ea17c in / 
# Wed, 17 Nov 2021 02:40:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:26:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:26:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 21:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 22:00:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 17 Nov 2021 22:00:45 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 17 Nov 2021 22:00:46 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 22:00:47 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 22:00:48 GMT
ENV JAVA_VERSION=8u312
# Wed, 17 Nov 2021 22:00:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 18 Nov 2021 06:49:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 18 Nov 2021 06:49:23 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 06:49:24 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 18 Nov 2021 06:49:25 GMT
WORKDIR /usr/local/tomcat
# Thu, 18 Nov 2021 06:49:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 18 Nov 2021 06:49:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 18 Nov 2021 06:57:22 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 18 Nov 2021 06:57:22 GMT
ENV TOMCAT_MAJOR=9
# Thu, 18 Nov 2021 06:57:23 GMT
ENV TOMCAT_VERSION=9.0.55
# Thu, 18 Nov 2021 06:57:24 GMT
ENV TOMCAT_SHA512=a0c480b8bba09069bda3b57f54e658450a59d799474ad587dead0ffbf5074c16ee3f9f9c13312d0ff3227c7034589dabf25941fbd672838e9baeee9661e024dc
# Thu, 18 Nov 2021 06:57:26 GMT
COPY dir:6ddaa5907c6fed72838e95bd41cbc4f5fd0a972bad6c7cfc210180a9d75f8dea in /usr/local/tomcat 
# Thu, 18 Nov 2021 06:57:29 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 06:57:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 18 Nov 2021 06:57:32 GMT
EXPOSE 8080
# Thu, 18 Nov 2021 06:57:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ce18cd0ba11c2dfa8c1a2d2b325e1e019b14d4ae25ffdeffb0f9686c5496bf5c`  
		Last Modified: Wed, 17 Nov 2021 02:46:45 GMT  
		Size: 53.6 MB (53619024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f138a340a2373acc72dcc4ea9ef08bdf5648aabc5fe08f7e8d25222ca63b7ee`  
		Last Modified: Wed, 17 Nov 2021 13:36:26 GMT  
		Size: 4.9 MB (4937639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34c030205ccb8656e30a58f96bb1edbe7c59bf17f3329ae3c442ec897f2b270`  
		Last Modified: Wed, 17 Nov 2021 13:36:27 GMT  
		Size: 10.7 MB (10655878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cda574254477c28979f32127ceea6240baf5deb81f044ae6047d126443eaf8f`  
		Last Modified: Wed, 17 Nov 2021 22:14:32 GMT  
		Size: 5.6 MB (5647104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2efe376834a50572ad7d98f5e73db772217f69ceefd7105b9cd6985d2f9835`  
		Last Modified: Wed, 17 Nov 2021 22:16:32 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15e77db3300f37b56dcc273cd6d42a92e2e9e91987c026884fe03c1c81565ef`  
		Last Modified: Wed, 17 Nov 2021 22:16:38 GMT  
		Size: 40.6 MB (40625387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034cd206624dcbc4c51a9c6e92fb46dc3cb0774f2bcae00db4c69c3c7a5cd957`  
		Last Modified: Thu, 18 Nov 2021 07:43:42 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53eef57d07c95c00d2fe3fa45c2a86c4cb133673b48d476b7c43250c7668677a`  
		Last Modified: Thu, 18 Nov 2021 07:49:33 GMT  
		Size: 12.2 MB (12167628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd32264e414de72c4b5354ee4e883ad884c963a05fff1b8967751002e6473b43`  
		Last Modified: Thu, 18 Nov 2021 07:49:32 GMT  
		Size: 217.0 KB (216959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
