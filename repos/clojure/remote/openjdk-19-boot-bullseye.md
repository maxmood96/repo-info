## `clojure:openjdk-19-boot-bullseye`

```console
$ docker pull clojure@sha256:fe38f9c52f96fdf21b378b342013ea631c0b24e652b3cb469dee7cb2b8106c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-19-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0d522daff152c0b04f09be284735216294f33570ee5443af7e59a8bb195a09e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 MB (392616600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565cd8197e068ecc4e5a5d9e31c6b7140a7ab93b06b028d0ce81a3c7eb447316`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:15 GMT
ADD file:9c4db2a9644ee3029a8e9cca58350efef660c3167e59b91f2bee9c303e592664 in / 
# Tue, 01 Mar 2022 02:13:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:26:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 06:26:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:20:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:20:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 14:20:32 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 14:20:32 GMT
ENV LANG=C.UTF-8
# Mon, 14 Mar 2022 20:14:38 GMT
ENV JAVA_VERSION=19-ea+13
# Mon, 14 Mar 2022 20:14:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6aff2a07ccdd649641741facf16a0001568e7af829e0e8cbd1257db42b6911f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2b13aabf01d1fad49c3dd5cde37bb53683a97b33d3d58030c10e1fad270f8c76'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Mar 2022 20:14:49 GMT
CMD ["jshell"]
# Mon, 14 Mar 2022 20:45:47 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 14 Mar 2022 20:45:47 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 14 Mar 2022 20:45:47 GMT
WORKDIR /tmp
# Mon, 14 Mar 2022 20:45:51 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Mon, 14 Mar 2022 20:45:51 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 14 Mar 2022 20:45:51 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 14 Mar 2022 20:46:35 GMT
RUN boot
# Mon, 14 Mar 2022 20:46:35 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 14 Mar 2022 20:46:36 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 14 Mar 2022 20:46:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e4d61adff2077d048c6372d73c41b0bd68f525ad41f5530af05098a876683055`  
		Last Modified: Tue, 01 Mar 2022 02:18:55 GMT  
		Size: 54.9 MB (54917063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff1945c672b08a1791df62afaaf8aff14d3047155365f9c3646902937f7ffe6`  
		Last Modified: Tue, 01 Mar 2022 06:36:13 GMT  
		Size: 5.2 MB (5153034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5b10aec998344606441aec43a335ab6326f32aae331aab27da16a6bb4ec2be`  
		Last Modified: Tue, 01 Mar 2022 06:36:14 GMT  
		Size: 10.9 MB (10871885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12de8c754e45686ace9e25d11bee372b070eed5b5ab20aa3b4fab8c936496d02`  
		Last Modified: Tue, 01 Mar 2022 06:36:38 GMT  
		Size: 54.6 MB (54575903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00199018d51876dde0db2a50f86b4db2ce5eaebcf284907dca80a8af67765bda`  
		Last Modified: Tue, 01 Mar 2022 14:40:10 GMT  
		Size: 14.1 MB (14071739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1ed8c70503e06348b37925dfbb45f52bfbee048d716f08cd6f53587b1ffffe`  
		Last Modified: Mon, 14 Mar 2022 20:23:00 GMT  
		Size: 193.2 MB (193188186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850a9651f54771924355a6244e4d6f4ebc6da0d137477ccd01d982860bc55af4`  
		Last Modified: Mon, 14 Mar 2022 20:51:57 GMT  
		Size: 1.0 MB (1017407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b13a53aa6efa863fb3245a5f8c7274eb91a66a6396a610aa95ab6e5eebee8c`  
		Last Modified: Mon, 14 Mar 2022 20:52:01 GMT  
		Size: 58.8 MB (58820976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93a7316ca1324f2239b5f7e978882a4a7706c6c95f9b7377699a16ea8d4027c`  
		Last Modified: Mon, 14 Mar 2022 20:51:57 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-19-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:05fae808f08f21395ae985bbda82f8739ce09301c84e671e32f6245d1a904d85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 MB (391424025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd011cea071ea34976034e1cfefd92d684086e27b45e1dffa194c55885347437`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:12 GMT
ADD file:9d66afa8fc90803d689e087b38b38a3bd58d0434b495ca4165ca520e73bccf55 in / 
# Tue, 01 Mar 2022 02:11:14 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:34:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 10:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:47:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:47:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 13:47:34 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 13:47:35 GMT
ENV LANG=C.UTF-8
# Mon, 14 Mar 2022 19:05:38 GMT
ENV JAVA_VERSION=19-ea+13
# Mon, 14 Mar 2022 19:05:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6aff2a07ccdd649641741facf16a0001568e7af829e0e8cbd1257db42b6911f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2b13aabf01d1fad49c3dd5cde37bb53683a97b33d3d58030c10e1fad270f8c76'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Mar 2022 19:05:48 GMT
CMD ["jshell"]
# Mon, 14 Mar 2022 19:58:36 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 14 Mar 2022 19:58:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 14 Mar 2022 19:58:38 GMT
WORKDIR /tmp
# Mon, 14 Mar 2022 19:58:42 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Mon, 14 Mar 2022 19:58:43 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 14 Mar 2022 19:58:44 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 14 Mar 2022 19:58:57 GMT
RUN boot
# Mon, 14 Mar 2022 19:58:58 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 14 Mar 2022 19:58:58 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 14 Mar 2022 19:58:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c7869242ae9abf6340558e18846f64a05eb06f2eaf66c6bfa2dc66ff2c997976`  
		Last Modified: Tue, 01 Mar 2022 02:17:52 GMT  
		Size: 53.6 MB (53608753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9880592b351f34fa791bd7749a127063cd6a76b1190bd059c168696d700f6b04`  
		Last Modified: Tue, 01 Mar 2022 10:44:26 GMT  
		Size: 5.1 MB (5141642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd9934a374f1ba93d2da0983d2aac86c9b4bf6ca063aa108519d2588e0212ac`  
		Last Modified: Tue, 01 Mar 2022 10:44:26 GMT  
		Size: 10.7 MB (10655864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37be3698694527b9e5af78494bbcb68f6b045af5247de8c988b24ef7dcd877e`  
		Last Modified: Tue, 01 Mar 2022 10:44:48 GMT  
		Size: 54.7 MB (54671139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5dc6dcc457fec75c4796decb43a2b4f5f0bfce35e577de9171e96fb39eeee4`  
		Last Modified: Tue, 01 Mar 2022 14:12:17 GMT  
		Size: 15.5 MB (15524992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8721790ef34835374c8cbfae43b79fcc71b5cba1dc6a16102e46ea0b431c5c`  
		Last Modified: Mon, 14 Mar 2022 19:20:01 GMT  
		Size: 192.2 MB (192228567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de96328dc612d3ad272f1709a184aedc832f8777365981d04f59f7db0522937e`  
		Last Modified: Mon, 14 Mar 2022 20:08:24 GMT  
		Size: 777.3 KB (777310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31bed1834bb96bb8e2df2df59e6416cdfe6df31c55e322a6f315479d04769f0`  
		Last Modified: Mon, 14 Mar 2022 20:08:29 GMT  
		Size: 58.8 MB (58815353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71f0184e2e6a97521ff7264bcc3d395dcc887fb512aa8a0d31ab7f8e8b1e5db`  
		Last Modified: Mon, 14 Mar 2022 20:08:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
