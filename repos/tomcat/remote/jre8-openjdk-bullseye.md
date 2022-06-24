## `tomcat:jre8-openjdk-bullseye`

```console
$ docker pull tomcat@sha256:492d227660592c356e008642ea8a059b69385425be62f1a6fb1a0c01cd8ed374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre8-openjdk-bullseye` - linux; amd64

```console
$ docker pull tomcat@sha256:a7466536aa7b463dcf98906330602ebbe74240081c643e1ae704e460b61b4fff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131090110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57bb5e03a227814388c0693bbfb5e01dcc58c1698a547c29417810bee5155dab`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:16 GMT
ADD file:798015650079cb88614ff181a30f9c3d3fde8361c49ae2dec2058d5a3e61f5df in / 
# Thu, 23 Jun 2022 00:20:16 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:50:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:50:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 04:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:01:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Jun 2022 05:01:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 05:01:22 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 05:01:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 05:01:22 GMT
ENV JAVA_VERSION=8u332
# Thu, 23 Jun 2022 05:01:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Jun 2022 22:44:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 23 Jun 2022 22:44:39 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 22:44:39 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 23 Jun 2022 22:44:40 GMT
WORKDIR /usr/local/tomcat
# Thu, 23 Jun 2022 22:44:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:44:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:44:40 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 23 Jun 2022 22:44:40 GMT
ENV TOMCAT_MAJOR=10
# Thu, 23 Jun 2022 22:44:40 GMT
ENV TOMCAT_VERSION=10.0.22
# Thu, 23 Jun 2022 22:44:40 GMT
ENV TOMCAT_SHA512=fe46db8794f066882b30e7a94bd8d3dbcf29e8e8ffaf67c1355846755745a7c9eafd124819283f218bcf410921a485b44b57b56fd6251fb99d67d95f3dd36826
# Thu, 23 Jun 2022 22:44:41 GMT
COPY dir:ea415ce3f81b72ed27a4c5777539e8bfe3aea64eb9e7fdc88dd180a779f7b64b in /usr/local/tomcat 
# Thu, 23 Jun 2022 22:44:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 22:44:46 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 23 Jun 2022 22:44:46 GMT
EXPOSE 8080
# Thu, 23 Jun 2022 22:44:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1339eaac5b67d16d6d9f41fb7a7b96f7cebf3ba4beab36cbb60935aa772af583`  
		Last Modified: Thu, 23 Jun 2022 00:24:48 GMT  
		Size: 55.0 MB (55009886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c78fa1b97999d08408734a61040475ade5bd7e33e91c0d5170dba2c7c7a92fd`  
		Last Modified: Thu, 23 Jun 2022 00:58:38 GMT  
		Size: 5.2 MB (5155961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f0d2bd524377dc42d072443c0e5e7cafa14f5df609d39bb1f717f43817a2cd`  
		Last Modified: Thu, 23 Jun 2022 00:58:38 GMT  
		Size: 10.9 MB (10875087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023992b49610b0f24fd4b80779987a1e9ed4a039f7a93c612a259c40f26d75f3`  
		Last Modified: Thu, 23 Jun 2022 05:18:22 GMT  
		Size: 5.7 MB (5657511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c157ac5e2cd4a56f16e8f79611a67fcda7bebc6cf1dd87de30cb8fcdecd5e4`  
		Last Modified: Thu, 23 Jun 2022 05:21:32 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b6fa2323bbb580f1865fca355dc5c76eb695d48205552c09a066b4be10ebe3`  
		Last Modified: Thu, 23 Jun 2022 05:21:37 GMT  
		Size: 41.4 MB (41424478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00be8419f55f0a199ad07b86c4bb4a5e7218f2f818b190961268a996e1f9af8d`  
		Last Modified: Thu, 23 Jun 2022 23:13:22 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78466ac15557bc029f17ad6e4853b7d7e123df216be3d85dee92ab7ab25292ff`  
		Last Modified: Thu, 23 Jun 2022 23:13:23 GMT  
		Size: 12.5 MB (12506996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd03ea42a78a72d838ea9b859a1d36b4bfa58874fbda84197d21bbf01de99875`  
		Last Modified: Thu, 23 Jun 2022 23:13:22 GMT  
		Size: 459.7 KB (459680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9848f8b6437ca02e1bab5b847c98bf81ab89d34180e8654fde4a1505d6d9842`  
		Last Modified: Thu, 23 Jun 2022 23:13:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-openjdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:003552c961e61495e1ec2361b6e170acc406988643f88e83fa4da4b7c37d2c20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128342124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67a2e78a3d2e5f2e7fc4aed4919e902859049dbb4f8aaf1ee409918a2de67c5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 28 May 2022 00:40:23 GMT
ADD file:a78273677555ebe8bac187f491203093eec62fa1c4f65f00ba2cf0cc2230992f in / 
# Sat, 28 May 2022 00:40:24 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 11:05:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 16:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 16:52:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 16:52:27 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 16:52:28 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 16:52:29 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 16:52:30 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 16:52:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 28 May 2022 20:13:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 28 May 2022 20:13:59 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 20:14:00 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 28 May 2022 20:14:01 GMT
WORKDIR /usr/local/tomcat
# Sat, 28 May 2022 20:14:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 20:14:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 20:14:04 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 28 May 2022 20:14:05 GMT
ENV TOMCAT_MAJOR=10
# Mon, 13 Jun 2022 21:07:06 GMT
ENV TOMCAT_VERSION=10.0.22
# Mon, 13 Jun 2022 21:07:07 GMT
ENV TOMCAT_SHA512=fe46db8794f066882b30e7a94bd8d3dbcf29e8e8ffaf67c1355846755745a7c9eafd124819283f218bcf410921a485b44b57b56fd6251fb99d67d95f3dd36826
# Mon, 13 Jun 2022 21:07:09 GMT
COPY dir:d3af460986c233ac9ee48f8239674603811f8a8ef8a7a183944b5f794184e849 in /usr/local/tomcat 
# Mon, 13 Jun 2022 21:07:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Jun 2022 21:07:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 13 Jun 2022 21:07:15 GMT
EXPOSE 8080
# Mon, 13 Jun 2022 21:07:16 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d794814721d57f8aaec06ab3652e90212cc3beccf5ff5c87f6ecf8375784bcc8`  
		Last Modified: Sat, 28 May 2022 00:47:04 GMT  
		Size: 53.7 MB (53696947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf62ee63325dbbad699d6845f68c2391db3bf158f60373849c2d1cb6bb479788`  
		Last Modified: Sat, 28 May 2022 11:17:05 GMT  
		Size: 4.9 MB (4938744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e37b4c58dd1db7ead6f3c2cdf757f490b4e29c958d2a70559c313e9a03a5ef`  
		Last Modified: Sat, 28 May 2022 11:17:06 GMT  
		Size: 10.7 MB (10657073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29312e2f0b2d2423a19b1e65da0020d22da272698007d994eb022cafc68c98dc`  
		Last Modified: Sat, 28 May 2022 17:06:29 GMT  
		Size: 5.6 MB (5649779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19e7746c6e90474872ec5be85df08b653cd2bdac1ada365c689b6170991983b`  
		Last Modified: Sat, 28 May 2022 17:08:32 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f891a8416b71c72bf9759a240d929eacfb0e4c3323cdbd74ffe2d4b62457d2`  
		Last Modified: Sat, 28 May 2022 17:08:37 GMT  
		Size: 40.7 MB (40664901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240385c5b2349ff81c49fd4ad69566993477d11fc2def21180c8357f813d7434`  
		Last Modified: Sat, 28 May 2022 21:01:52 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d2a9f91ccfbfc885ef21e0c5b727b9e7586b08920159f2dcb58301a4cff733`  
		Last Modified: Mon, 13 Jun 2022 21:50:38 GMT  
		Size: 12.5 MB (12517169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c710d25b5354ad95665c94543cc5ec38a45c630964369cdc4d129470a8c0fe`  
		Last Modified: Mon, 13 Jun 2022 21:50:36 GMT  
		Size: 217.2 KB (217163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
