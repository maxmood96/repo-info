## `clojure:boot-bullseye`

```console
$ docker pull clojure@sha256:df2ab38f991e69564b70a199f3635a56c1da458c85538b62c5f6f1ada711defc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f1bbcd766df1de5ab4145ca2d5671c728a27fe3034b6da40a450b745a7979256
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.7 MB (385704686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f45e5b347b7514ab474d88d6b7a937284a90b4397c10deed00fc24bf726fc10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:07 GMT
ADD file:e777355768c63f735e5458c7e0ada7f556f27d0493b3af35dc7c34f9c4294ea9 in / 
# Thu, 02 Dec 2021 02:48:08 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:39:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:40:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:28:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:32:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Thu, 02 Dec 2021 11:32:01 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:32:01 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:32:01 GMT
ENV JAVA_VERSION=17.0.1
# Thu, 02 Dec 2021 11:32:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:32:19 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 13:11:40 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 03 Dec 2021 13:11:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 03 Dec 2021 13:11:40 GMT
WORKDIR /tmp
# Fri, 03 Dec 2021 13:11:42 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Fri, 03 Dec 2021 13:11:42 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 03 Dec 2021 13:11:42 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 03 Dec 2021 13:12:06 GMT
RUN boot
# Fri, 03 Dec 2021 13:12:06 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 03 Dec 2021 13:12:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 03 Dec 2021 13:12:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5e0b432e8ba9d9029a000e627840b98ffc1ed0c5172075b7d3e869be0df0fe9b`  
		Last Modified: Thu, 02 Dec 2021 02:53:18 GMT  
		Size: 54.9 MB (54932878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84cfd68b5cea612a8343c346bfa5bd6c486769010d12f7ec86b23c74887feb2`  
		Last Modified: Thu, 02 Dec 2021 03:49:22 GMT  
		Size: 5.2 MB (5153424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8f2315954535f1e27cd13d777e73da4a787b0aebf4241d225beff3c91cbb1`  
		Last Modified: Thu, 02 Dec 2021 03:49:23 GMT  
		Size: 10.9 MB (10871995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598fa43a7e793a76c198e8d45d8810394e1cfc943b2673d7fcf5a6fdc4f45b3`  
		Last Modified: Thu, 02 Dec 2021 03:49:46 GMT  
		Size: 54.6 MB (54567844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718dc22cae0d908da735cfc9f467980c8c89a8029b7fe88b1f442d6df8c8a305`  
		Last Modified: Thu, 02 Dec 2021 11:46:40 GMT  
		Size: 14.1 MB (14071762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07a790fa7e7c86fdd71d279b6e5deeb25d3115585feeba6eb938dadcdac2fe4`  
		Last Modified: Thu, 02 Dec 2021 11:50:58 GMT  
		Size: 187.3 MB (187278953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f79f553780c7e992ca87d432eb77bbcdf6d4a111c813b27bcee562c14dc4af`  
		Last Modified: Fri, 03 Dec 2021 13:29:09 GMT  
		Size: 6.9 KB (6892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e076f4afbabe57472e52cbc3a9f47d0d8ab1d781ff8d57a3a1d6986f6923e8bc`  
		Last Modified: Fri, 03 Dec 2021 13:29:13 GMT  
		Size: 58.8 MB (58820532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2fb805400163a56de0215bc6da17a6f7dc9d45fa28289f65fd82ffec9ec8448`  
		Last Modified: Fri, 03 Dec 2021 13:29:09 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:50852982bc1cfff659dff017e91f516e53207506dea687f4955ae5a39ddfec3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384504313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc7cf8ba2665e657b7572387b235ca0c6b02d0198195b870f27f929e9058c7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:08 GMT
ADD file:9d88e8701cd12aaee44dac3542cc3e4586f6382541afff76e56e8fb5275387d3 in / 
# Tue, 21 Dec 2021 01:42:09 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:12:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:52:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:57:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 21 Dec 2021 02:57:34 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:57:35 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 02:57:36 GMT
ENV JAVA_VERSION=17.0.1
# Tue, 21 Dec 2021 02:57:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 02:57:49 GMT
CMD ["jshell"]
# Tue, 21 Dec 2021 22:19:47 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Dec 2021 22:19:47 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Dec 2021 22:19:48 GMT
WORKDIR /tmp
# Tue, 21 Dec 2021 22:19:50 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Tue, 21 Dec 2021 22:19:50 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Dec 2021 22:19:51 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Dec 2021 22:20:05 GMT
RUN boot
# Tue, 21 Dec 2021 22:20:06 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 21 Dec 2021 22:20:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Dec 2021 22:20:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:94a23d3cb5be24659b25f17537307e7f568d665244f6a383c1c6e51e31080749`  
		Last Modified: Tue, 21 Dec 2021 01:48:23 GMT  
		Size: 53.6 MB (53604608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9d381bd1e98fa8759f80ff42db63c8fce4ac9407b2e7c8e0f031ed9f96432b`  
		Last Modified: Tue, 21 Dec 2021 02:22:29 GMT  
		Size: 5.1 MB (5141526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9c5b49b9db3dd2553e8ae6c2081b77274ec0a8b1f9903b0e5ac83900642098`  
		Last Modified: Tue, 21 Dec 2021 02:22:30 GMT  
		Size: 10.7 MB (10655891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841dd868500b6685b6cda93c97ea76e817b427d7a10bf73e9d03356fac199ffd`  
		Last Modified: Tue, 21 Dec 2021 02:22:52 GMT  
		Size: 54.7 MB (54668906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6575128af71feb3eba6809b36717cd9a918ad4434aa65d121f228313ad6c2fc1`  
		Last Modified: Tue, 21 Dec 2021 03:15:17 GMT  
		Size: 15.5 MB (15525097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c385b89db90b7b7b97633cfae8fdf1241537b93a91b615c8ac557f6a6015b1e`  
		Last Modified: Tue, 21 Dec 2021 03:22:16 GMT  
		Size: 186.1 MB (186085317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc1f1c28c95572e4c6dab314689219edeb90a9452deeec37109834e9e7abc43`  
		Last Modified: Tue, 21 Dec 2021 22:41:42 GMT  
		Size: 6.9 KB (6873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d75f530d494a6582376e3d1ba083e9d1ff54591ca50c7914641be450836ca7`  
		Last Modified: Tue, 21 Dec 2021 22:41:47 GMT  
		Size: 58.8 MB (58815689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b0f31c43b981fbe3959f5d77f9c7cf7489593a3a36469f30bc1025cfc76106`  
		Last Modified: Tue, 21 Dec 2021 22:41:43 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
