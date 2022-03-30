## `clojure:openjdk-11-boot-bullseye`

```console
$ docker pull clojure@sha256:d2199c53e6668f779b419369fcbbe0a15b5e50ee535ad2b36219deed3e1f42ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3bbe98ba7e77ca470f33ed937be0d93b99e409700b70cce2b70220fa6bc97cfc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.1 MB (394053903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea5e6571bc216ccc1408e1ddce077b0edc75c6c38ecfa702e892c28ddb1b582`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:07 GMT
ADD file:e8d512b08fe2ddc6f2c85831c73e4c72b9c850fa428913d19da4bb1a34f84cf2 in / 
# Tue, 29 Mar 2022 00:22:08 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:29:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:29:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 17:30:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:11:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:11:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 29 Mar 2022 23:11:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 29 Mar 2022 23:11:15 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 23:11:15 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 23:11:16 GMT
ENV JAVA_VERSION=11.0.14.1
# Tue, 29 Mar 2022 23:11:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 23:11:28 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:46:15 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 29 Mar 2022 23:46:15 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 29 Mar 2022 23:46:16 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:46:19 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Tue, 29 Mar 2022 23:46:19 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 29 Mar 2022 23:46:19 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 29 Mar 2022 23:46:44 GMT
RUN boot
# Tue, 29 Mar 2022 23:46:44 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:dbba69284b2786013fe94fefe0c2e66a7d3cecbb20f6d691d71dac891ee37be5`  
		Last Modified: Tue, 29 Mar 2022 00:26:47 GMT  
		Size: 54.9 MB (54937710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9baf437a1badb6aad2dae5f2cd4a7b53a6c7ab6c14cba1ed1ecb42b4822b0e87`  
		Last Modified: Tue, 29 Mar 2022 17:38:08 GMT  
		Size: 5.2 MB (5155705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ade5c59e324bd7cf369c72ad781c23d37e8fb48c9bbb4abbecafafd9be4cc35`  
		Last Modified: Tue, 29 Mar 2022 17:38:08 GMT  
		Size: 10.9 MB (10874957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19a994f6d4cdbb620339bd2e4ad47b229f14276b542060622ae447649294e5d`  
		Last Modified: Tue, 29 Mar 2022 17:38:33 GMT  
		Size: 54.6 MB (54576420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c0aceedb57f6288702dbed4b3a98c5274bc4c3fd4ed116f2d2489e3164012f`  
		Last Modified: Tue, 29 Mar 2022 23:27:15 GMT  
		Size: 5.4 MB (5420160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e7c71ec633cf1303e720faf8462da622fe499c4f5a44c0a01cc01a3aeaacc1`  
		Last Modified: Tue, 29 Mar 2022 23:27:14 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612cf131e4880254616bc7da37ab4270993efc252ffbe022f98c49b6b64841b4`  
		Last Modified: Tue, 29 Mar 2022 23:27:29 GMT  
		Size: 203.3 MB (203253348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee4fc1283c962fdb91a91f58d243c686293240ce7bf567489fb55304f5e5028`  
		Last Modified: Wed, 30 Mar 2022 00:06:20 GMT  
		Size: 1.0 MB (1014874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d514a92fbc9c190234d4a4462ba993516352406c671ee3b4b5ffe9407f4b15fd`  
		Last Modified: Wed, 30 Mar 2022 00:06:24 GMT  
		Size: 58.8 MB (58820520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:747641da983edf52cf74ee6097826dccfcdbfa968be444301e4a6af76717510f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 MB (389774599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103d72fb409ff56ee9d0096f255f3d1d21c9d2ea4f74826e53a15389d1e8475a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 22:11:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 23:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 23:28:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 17 Mar 2022 23:28:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 17 Mar 2022 23:28:16 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 23:28:17 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 23:28:18 GMT
ENV JAVA_VERSION=11.0.14.1
# Thu, 17 Mar 2022 23:28:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 17 Mar 2022 23:28:55 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 09:05:50 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 19 Mar 2022 09:05:50 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 19 Mar 2022 09:05:51 GMT
WORKDIR /tmp
# Sat, 19 Mar 2022 09:05:55 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Sat, 19 Mar 2022 09:05:56 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 19 Mar 2022 09:05:57 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 19 Mar 2022 09:06:11 GMT
RUN boot
# Sat, 19 Mar 2022 09:06:12 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399f445da611be3789923cf26d158e3f4f80449b7295fa069a8eaecaaf137e6`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 4.9 MB (4937558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9e43777fa6c09c341f3aa922f47b5b3ace26de1d779124afd2f1d435731d9`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 10.7 MB (10655858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81267e40a2df9e572fe797e45dbc086008422eb2216df18b7a91f1cf13e22b`  
		Last Modified: Thu, 17 Mar 2022 22:21:21 GMT  
		Size: 54.7 MB (54671322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13257f99de62ae8cc7fb7ff399b0ee6571e084300f5bf732624b1442497e9151`  
		Last Modified: Thu, 17 Mar 2022 23:55:40 GMT  
		Size: 5.4 MB (5420241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e3ccfe41671b9527cc200d8b1dbbc0b7ae3cc6d1b281195a4158bd7f302466`  
		Last Modified: Thu, 17 Mar 2022 23:55:39 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ec98e8e02788e85d3d5c4aea735378f011b8f3aec53d8389227b0cb314fc9c`  
		Last Modified: Thu, 17 Mar 2022 23:55:56 GMT  
		Size: 200.9 MB (200882222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cc971e6f93c89aa2c4cb221416c3e8adfd376a025c4990721740cb578a7158`  
		Last Modified: Sat, 19 Mar 2022 09:30:27 GMT  
		Size: 775.5 KB (775471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c8b2ac45ca565b77032bf4899cc2166112cd877bc2f97b4cf094fc941e4293`  
		Last Modified: Sat, 19 Mar 2022 09:30:34 GMT  
		Size: 58.8 MB (58815410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
