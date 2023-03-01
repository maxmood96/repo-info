## `openjdk:21-jdk-bullseye`

```console
$ docker pull openjdk@sha256:4af2a3fbf84856c9a59c9f62c9fac70338c5e5feb1be3546afa2387bd5d8a374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:f14ea2e7afb61f69ad016cdfb96b742056ade8d6771d70b885ff16c7ca47168d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339219293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74204f5cb6ccd44919f7bd93fafdccab0f171a9a3549c315e4cc8885b503bb4f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:05 GMT
ADD file:b03d13d345c29f69557f410c8504e748226756d1f48e5abdb63cd40179b2640c in / 
# Thu, 09 Feb 2023 03:20:05 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:10:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:10:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 09:11:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:46:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:46:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Thu, 09 Feb 2023 10:46:56 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 10:46:56 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2023 01:30:19 GMT
ENV JAVA_VERSION=21-ea+11
# Tue, 28 Feb 2023 01:30:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='44d5639ae3005e8f6a494ab42506f7fbbe7c366a17c7da792bcaf21a04f5be13'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4f1bfbab4042464ed8c0b6e462354db5e97320b7c74d257639fc4c05d3ce4827'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Feb 2023 01:30:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e4aec178e0864db93a6f97a20bde3445871a4562c1801185eca1238d3a0e80d`  
		Last Modified: Thu, 09 Feb 2023 03:24:47 GMT  
		Size: 55.0 MB (55046771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1024729feeb2893dad43684fe7679c4d866c3640dfc3912bbd93c5a51f32d2`  
		Last Modified: Thu, 09 Feb 2023 09:17:56 GMT  
		Size: 5.2 MB (5165984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aa11fbc85a2a9660c98cfb4d0a2db8cde983ce3c87565c356cfdf1ddf2654c`  
		Last Modified: Thu, 09 Feb 2023 09:17:56 GMT  
		Size: 10.9 MB (10876805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa54add66b3a47555c8b761f60b15f818236cc928109a30032111efc98c6fcd4`  
		Last Modified: Thu, 09 Feb 2023 09:18:15 GMT  
		Size: 54.6 MB (54587652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424a482a242625bf23d28ac754f5a65ffc1365d58a9c2f254bb8403169077fe0`  
		Last Modified: Thu, 09 Feb 2023 10:53:37 GMT  
		Size: 14.1 MB (14072070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ff9601a1757f0fa86a9236fc19c2a45a48a41d38738067c309bee4d8bbfcb0`  
		Last Modified: Tue, 28 Feb 2023 01:34:29 GMT  
		Size: 199.5 MB (199470011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b3bf4d26ca86bdf302e583a4b8b03d18806b3a49ed7f5e872cab9b95a61fcd25
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337894652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b137fe87dd90bc5cdbfbd2d48d10fa54bcd25c189b2a6cffab870738349abf`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:49:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:49:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 02:49:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:24:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:24:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 01 Mar 2023 05:24:05 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:24:05 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 05:24:06 GMT
ENV JAVA_VERSION=21-ea+11
# Wed, 01 Mar 2023 05:24:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='44d5639ae3005e8f6a494ab42506f7fbbe7c366a17c7da792bcaf21a04f5be13'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4f1bfbab4042464ed8c0b6e462354db5e97320b7c74d257639fc4c05d3ce4827'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 01 Mar 2023 05:24:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8a090f23f28b92f40160bc1a686e3bd5cd4bbd00713a7133631cb2189575f2`  
		Last Modified: Wed, 01 Mar 2023 02:56:19 GMT  
		Size: 5.2 MB (5152682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec29ff8525a3f037f4cc74d2925846a9a8c985469b4ae98fa34099110288987c`  
		Last Modified: Wed, 01 Mar 2023 02:56:19 GMT  
		Size: 10.9 MB (10873588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8747d4a988af1d119e668971a87213d5c7061fc04671ba6fcb7123a1c11507ac`  
		Last Modified: Wed, 01 Mar 2023 02:56:37 GMT  
		Size: 54.7 MB (54676365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2969501ead1184d760cf0942308575ccdfc426c362fee4acfe6c6fd6d7b309`  
		Last Modified: Wed, 01 Mar 2023 05:28:01 GMT  
		Size: 15.5 MB (15529086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f539336cb7533a3c11a6985fc4fa2f729660c4c15fd609596d017d499c7cbc2b`  
		Last Modified: Wed, 01 Mar 2023 05:28:11 GMT  
		Size: 198.0 MB (197959716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
