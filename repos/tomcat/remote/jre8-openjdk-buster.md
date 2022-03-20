## `tomcat:jre8-openjdk-buster`

```console
$ docker pull tomcat@sha256:1e11ac880dedb6ba5b24744300199298291558b18d9d9530d968ea3def70fd64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre8-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:56e85338951a24b6c15468ec658a6eaa2d1c9c55a9e74a191ebf71e2e80cb813
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128194420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135797ef784f74b58a0cd6ff78dd5ad8c078f20e504203615eb4be5a554691dd`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 10:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:30:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 19 Mar 2022 10:30:09 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 19 Mar 2022 10:30:09 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:30:09 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:30:09 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:30:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sun, 20 Mar 2022 11:26:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sun, 20 Mar 2022 11:26:35 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Mar 2022 11:26:36 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sun, 20 Mar 2022 11:26:36 GMT
WORKDIR /usr/local/tomcat
# Sun, 20 Mar 2022 11:26:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sun, 20 Mar 2022 11:26:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sun, 20 Mar 2022 11:26:36 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sun, 20 Mar 2022 11:26:36 GMT
ENV TOMCAT_MAJOR=10
# Sun, 20 Mar 2022 11:26:36 GMT
ENV TOMCAT_VERSION=10.0.18
# Sun, 20 Mar 2022 11:26:36 GMT
ENV TOMCAT_SHA512=a9e3c516676369bd9d52e768071898b0e07659a9ff03b9dc491e53f084b9981a929bf2c74a694f06ad26dae0644fb9617cc6e364f0e1dcd953c857978a95a644
# Sun, 20 Mar 2022 11:26:37 GMT
COPY dir:ea7ed044349e8e1219649ea578a3fc3724e0324ffdfb34b07dbc3a1fe83118cf in /usr/local/tomcat 
# Sun, 20 Mar 2022 11:26:41 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sun, 20 Mar 2022 11:26:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sun, 20 Mar 2022 11:26:42 GMT
EXPOSE 8080
# Sun, 20 Mar 2022 11:26:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eaf79a044669ac4a77db074212e085e5f13aec085e1f08050790cb04aad920`  
		Last Modified: Sat, 19 Mar 2022 10:46:20 GMT  
		Size: 5.5 MB (5532255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961b2b1ebb1dc930fa5954e4bf790035c372c34f69b5aaa9e484c981cc9b8105`  
		Last Modified: Sat, 19 Mar 2022 10:49:04 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f945d937f010be456d4f4e06aba96eff5c3520c5b2c85116c31a9bb2bcc60be`  
		Last Modified: Sat, 19 Mar 2022 10:49:11 GMT  
		Size: 41.4 MB (41395069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093eb01f1b677e9aebc8f4c93fe4d8c21cfcd72a6942851be8dfa4b95cba49da`  
		Last Modified: Sun, 20 Mar 2022 12:17:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259b151b0e17393597feb6d0cd57c757c3f062d57ed2f8f042b94e5720f9703e`  
		Last Modified: Sun, 20 Mar 2022 12:17:29 GMT  
		Size: 12.5 MB (12537012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9f21c86d312eef62bf415b45ca3a7b73ec16e727d7bfb7a2d5d50b5c0cddd7`  
		Last Modified: Sun, 20 Mar 2022 12:17:29 GMT  
		Size: 460.9 KB (460879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e138f18377bb463c95b7622bc9a8daf20489aac1a7da3639d113eddff85938cd`  
		Last Modified: Sun, 20 Mar 2022 12:17:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:7fcc3c613a2d8b29ad39064844b843870cfd1dae686a3263176c8d78d48d149b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125621160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da553a06979f807248b4342df47ff279904ae894b6b641919e02d52c114bc3b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:08 GMT
ADD file:37cabd1fec04269c22fc158f62ce5bc655934f2e58fb1ff3a1e366a33ba9bc18 in / 
# Thu, 17 Mar 2022 03:22:09 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:12:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 23:33:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 23:37:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 17 Mar 2022 23:37:41 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 17 Mar 2022 23:37:42 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 23:37:43 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 23:37:44 GMT
ENV JAVA_VERSION=8u322
# Thu, 17 Mar 2022 23:37:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 19 Mar 2022 11:31:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 19 Mar 2022 11:31:18 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 11:31:19 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 19 Mar 2022 11:31:20 GMT
WORKDIR /usr/local/tomcat
# Sat, 19 Mar 2022 11:31:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 11:31:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 19 Mar 2022 11:31:23 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 19 Mar 2022 11:31:24 GMT
ENV TOMCAT_MAJOR=10
# Sat, 19 Mar 2022 11:31:25 GMT
ENV TOMCAT_VERSION=10.0.18
# Sat, 19 Mar 2022 11:31:26 GMT
ENV TOMCAT_SHA512=a9e3c516676369bd9d52e768071898b0e07659a9ff03b9dc491e53f084b9981a929bf2c74a694f06ad26dae0644fb9617cc6e364f0e1dcd953c857978a95a644
# Sat, 19 Mar 2022 11:31:28 GMT
COPY dir:7b54a6d1a96d0e00918c0e1e281cc36584ad33864e2740a6155a170465a6528d in /usr/local/tomcat 
# Sat, 19 Mar 2022 11:31:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 11:31:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 19 Mar 2022 11:31:34 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 11:31:35 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3996f04b7c6c17d8b25c04c7287353b896b4a0b10ab440f47d00573a7d5c3e17`  
		Last Modified: Thu, 17 Mar 2022 03:28:59 GMT  
		Size: 49.2 MB (49222993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80907b498681187ef4aa817ec6f39ba351e376afbb4fcf4415841ab9015cfc59`  
		Last Modified: Thu, 17 Mar 2022 22:22:15 GMT  
		Size: 7.7 MB (7695349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8327dc7899c1a628cf11f95bb594fca3c86e45d1f4f0eb73d2ba9058eba5927`  
		Last Modified: Thu, 17 Mar 2022 22:22:15 GMT  
		Size: 9.8 MB (9767203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c8cde2d5e9d31d1b6eddddf3ae8e11b9d09f2a5a27bf2a825be248088e76a3`  
		Last Modified: Fri, 18 Mar 2022 00:00:18 GMT  
		Size: 5.5 MB (5506222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28b1a3c630183836ef1838d016b5f0f97e467700194e16f84cc4ba76a1934fc`  
		Last Modified: Fri, 18 Mar 2022 00:03:52 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a668d7a2d60b4d80e69ef05b92584aea9a6ae49ebb919f2126c4f4b0a496fc85`  
		Last Modified: Fri, 18 Mar 2022 00:03:57 GMT  
		Size: 40.7 MB (40659858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3d7ec91ac8a38fc6d36356fd0da7cfc5a06a4752dcfcb3dbfe10c809e93774`  
		Last Modified: Sat, 19 Mar 2022 12:39:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff54667147c8c92b8fac1016baf3ef6b209812e575084f51152dcd6f6d73c33`  
		Last Modified: Sat, 19 Mar 2022 12:39:10 GMT  
		Size: 12.6 MB (12550986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93aa181162c55f4e78b18f68649145f1c7b853d466bab8170c6dc2cc37c87cc`  
		Last Modified: Sat, 19 Mar 2022 12:39:08 GMT  
		Size: 218.2 KB (218201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
