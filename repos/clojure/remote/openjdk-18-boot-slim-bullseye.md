## `clojure:openjdk-18-boot-slim-bullseye`

```console
$ docker pull clojure@sha256:5663de3e792da916d75dcb24672fbfacf4b025aed484eb7ec18b7ec2d3368434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-slim-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e5f15f4a91109732c3c39ba54b5065757da8ed4e5515677f26efcdd50041f3d4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (280989593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5d173b20d72e1512bd31ee417bdaf044794da11c561a67a9f0d64dab791121`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:29:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Thu, 02 Dec 2021 11:29:27 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:29:27 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:29:27 GMT
ENV JAVA_VERSION=18-ea+25
# Thu, 02 Dec 2021 11:29:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/25/GPL/openjdk-18-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='74a01fc91a33136b6a5d387ecdfc2790ef5e351e3bef869706b288bc9a1df6a2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/25/GPL/openjdk-18-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f6f03a12f2c2228a46544ba43b73cd40e4bbb7b5ef857445641d64391d04798c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:29:51 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 13:13:25 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 03 Dec 2021 13:13:25 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 03 Dec 2021 13:13:25 GMT
WORKDIR /tmp
# Fri, 03 Dec 2021 13:13:30 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 03 Dec 2021 13:13:30 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 03 Dec 2021 13:13:30 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 03 Dec 2021 13:13:51 GMT
RUN boot
# Fri, 03 Dec 2021 13:13:51 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 03 Dec 2021 13:13:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 03 Dec 2021 13:13:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9f5b9b70c2f137dc70e816256e7a568a084d066e7c34c028d30a6a45438685`  
		Last Modified: Thu, 02 Dec 2021 11:47:20 GMT  
		Size: 1.6 MB (1582045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19176c56743ed66962a13dca568169b0ad179a118077121d4e0198f14f0421a2`  
		Last Modified: Thu, 02 Dec 2021 11:47:40 GMT  
		Size: 188.9 MB (188933389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214fdf22b3df7a1226b32133c68b70e750b092af51d2867fee0863170067b027`  
		Last Modified: Fri, 03 Dec 2021 13:30:47 GMT  
		Size: 283.1 KB (283084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127b3a38f84b82bfd573cf99d68f54b39ec7a94b800c4e4969017c5226a34bed`  
		Last Modified: Fri, 03 Dec 2021 13:30:50 GMT  
		Size: 58.8 MB (58820448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8f9ac0b2e5c4b78b1dcd5b6124f29505bf405832eb748c300b3370398a40e6`  
		Last Modified: Fri, 03 Dec 2021 13:30:47 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5c1ce53e51423f487c3273102719700d1042432c94c5f81223ca72c5f499b402
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (277957934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e2cd0aad8454f863385313c388758b1d22a5ab40fa1e3dc553564873d76314`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:02:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:02:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Thu, 02 Dec 2021 11:02:15 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:02:16 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 11:02:17 GMT
ENV JAVA_VERSION=18-ea+25
# Thu, 02 Dec 2021 11:02:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/25/GPL/openjdk-18-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='74a01fc91a33136b6a5d387ecdfc2790ef5e351e3bef869706b288bc9a1df6a2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/25/GPL/openjdk-18-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f6f03a12f2c2228a46544ba43b73cd40e4bbb7b5ef857445641d64391d04798c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 02 Dec 2021 11:02:34 GMT
CMD ["jshell"]
# Fri, 03 Dec 2021 06:03:54 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 03 Dec 2021 06:03:55 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 03 Dec 2021 06:03:56 GMT
WORKDIR /tmp
# Fri, 03 Dec 2021 06:04:01 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 03 Dec 2021 06:04:01 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 03 Dec 2021 06:04:02 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 03 Dec 2021 06:04:18 GMT
RUN boot
# Fri, 03 Dec 2021 06:04:19 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 03 Dec 2021 06:04:19 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 03 Dec 2021 06:04:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595058421fcb005f80f2faa2434369885cb20645caed265e7b4912808701d893`  
		Last Modified: Thu, 02 Dec 2021 11:23:15 GMT  
		Size: 1.4 MB (1361242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4386140193ddc3fef7b1d04fb15e1048d1d298bec6711ade1bc97b269ffbe53`  
		Last Modified: Thu, 02 Dec 2021 11:23:33 GMT  
		Size: 187.7 MB (187656885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b945fad88b6adbfc2d281901830875bc80845c5d49f03e076381ba0bcfc77f2`  
		Last Modified: Fri, 03 Dec 2021 06:25:24 GMT  
		Size: 67.2 KB (67231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce2a66b35cd814727f3c87799a6ab8b91327f2ec01a66f2a00e0e369813fdb1`  
		Last Modified: Fri, 03 Dec 2021 06:25:31 GMT  
		Size: 58.8 MB (58815636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64a9f7716137ada1f9b2a05f0a6c88c4262e73991e931522f241171989dd380`  
		Last Modified: Fri, 03 Dec 2021 06:25:24 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
