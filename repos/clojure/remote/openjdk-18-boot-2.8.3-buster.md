## `clojure:openjdk-18-boot-2.8.3-buster`

```console
$ docker pull clojure@sha256:051d10e8d9fcb788c34fe3ccad5d37f267a032429861867f63070d931d06039f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-2.8.3-buster` - linux; amd64

```console
$ docker pull clojure@sha256:2c75c740faa92de8270285dda08d47d4bf6161489edf94305e07463d66b631da
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.6 MB (381602834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d35b78718af86fec98cb42189b36366c9288012b13d3d85932c1470da55469`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:53 GMT
ADD file:be998d04a8927e9c4b105995e3b9d6800ea798807389f7c5921c0f4774328e21 in / 
# Tue, 21 Dec 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:53:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 01:53:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 01:53:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 22:58:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 22:59:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 21 Dec 2021 22:59:42 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 22:59:42 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 22:59:42 GMT
ENV JAVA_VERSION=18-ea+28
# Tue, 21 Dec 2021 22:59:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='7e5f0e54c799f8c155a934e61d88f4fef3a70a641c1636c925158622c7bd9341'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='e29aa39763ebcfe5f037cc4fe47c6b9eb34cbe482f6ea57e93de89070255e22b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 22:59:54 GMT
CMD ["jshell"]
# Wed, 22 Dec 2021 13:41:39 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 22 Dec 2021 13:41:39 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 22 Dec 2021 13:41:39 GMT
WORKDIR /tmp
# Wed, 22 Dec 2021 13:41:40 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Wed, 22 Dec 2021 13:41:40 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Dec 2021 13:41:40 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 22 Dec 2021 13:42:03 GMT
RUN boot
# Wed, 22 Dec 2021 13:42:03 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 22 Dec 2021 13:42:03 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Dec 2021 13:42:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9b99af5931b39ce167150ad668cfa57ddf7664697be9996cb7e0e6aebbf05843`  
		Last Modified: Tue, 21 Dec 2021 01:28:07 GMT  
		Size: 50.4 MB (50437136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6013b3e77fe6fd3dcf46a05f8e5b3afa9fbca7ba0161c62e56beb4058334dec`  
		Last Modified: Tue, 21 Dec 2021 02:02:46 GMT  
		Size: 7.8 MB (7833863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbced17b6899896c8e4016d62c885d737fe667acace2733e17c64bb974232887`  
		Last Modified: Tue, 21 Dec 2021 02:02:46 GMT  
		Size: 10.0 MB (9997172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b609dabefa83fae157bcd42123a8ed45199bb6c301e09a11260c1cad9babfef`  
		Last Modified: Tue, 21 Dec 2021 02:03:05 GMT  
		Size: 51.8 MB (51841352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdedc4ba2f5e3c8c742aac0efd5bf20b6ff7b5777dcb5308ff111a3e4396d984`  
		Last Modified: Tue, 21 Dec 2021 23:15:30 GMT  
		Size: 13.9 MB (13921199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57775ea0e9af836f0beabfb938ac3d8146aff8011312ced9b8b2559d57de8ca6`  
		Last Modified: Tue, 21 Dec 2021 23:18:31 GMT  
		Size: 188.7 MB (188744355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa49e9946b1c3470715f5db5fac3b8aae804fd771b7242dceedb9971547bc32b`  
		Last Modified: Wed, 22 Dec 2021 14:00:13 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10a23158e069a1705f798632189c7f53ac857aa7f538ad1d1d05813939a1793`  
		Last Modified: Wed, 22 Dec 2021 14:00:16 GMT  
		Size: 58.8 MB (58820454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4be60f2a75ec51ec1613ef7f8310c4fd119007d34181b957c18e17b2c0e1257`  
		Last Modified: Wed, 22 Dec 2021 14:00:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-2.8.3-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ab6480db7d882ae1dedff05b6cfb882615aaacc76aef33b331d9d87143d5b767
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.0 MB (380036836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2506eded3bf7cf7753a32bb7e4a4058f98196d6353c72bc70a9768ba3e4c0b19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:34 GMT
ADD file:73bd5e773b257a6ea5d29845b2b112ebce468878a9467e7c0fe61c69994bb47f in / 
# Tue, 21 Dec 2021 01:42:35 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:13:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:13:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:14:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:56:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 21 Dec 2021 02:56:19 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:56:20 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 02:56:21 GMT
ENV JAVA_VERSION=18-ea+28
# Tue, 21 Dec 2021 02:56:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='7e5f0e54c799f8c155a934e61d88f4fef3a70a641c1636c925158622c7bd9341'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='e29aa39763ebcfe5f037cc4fe47c6b9eb34cbe482f6ea57e93de89070255e22b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 02:56:34 GMT
CMD ["jshell"]
# Tue, 21 Dec 2021 22:12:36 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Dec 2021 22:12:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Dec 2021 22:12:37 GMT
WORKDIR /tmp
# Tue, 21 Dec 2021 22:12:44 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Tue, 21 Dec 2021 22:12:44 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Dec 2021 22:12:45 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Dec 2021 22:12:59 GMT
RUN boot
# Tue, 21 Dec 2021 22:13:00 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 21 Dec 2021 22:13:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Dec 2021 22:13:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:741eb94195433e00f9799629cc66740c97d607d6f3ed207e5738995897c52959`  
		Last Modified: Tue, 21 Dec 2021 01:49:16 GMT  
		Size: 49.2 MB (49223144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d098cf33298807975a4d84f59f6689e0bf729b62fca9b7320adb80ebeaabc578`  
		Last Modified: Tue, 21 Dec 2021 02:23:45 GMT  
		Size: 7.7 MB (7695163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0317c7db28bd6855b787608d1f4236185907b452f6f545a9954be870828af6`  
		Last Modified: Tue, 21 Dec 2021 02:23:45 GMT  
		Size: 9.8 MB (9767165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4301bfae0dab5df877b31fde90c919b02335f783b7405d66b6123acfe03e69e`  
		Last Modified: Tue, 21 Dec 2021 02:24:05 GMT  
		Size: 52.2 MB (52168887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c1cf4e1d86834082c63f5bd67efeec8dccd801ae671f9bce3cdf6f178be4a9`  
		Last Modified: Tue, 21 Dec 2021 03:17:02 GMT  
		Size: 14.7 MB (14671031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21506560cbde4b659d6c901a19db7123b316fba126e8bb1df930b731509a32ad`  
		Last Modified: Tue, 21 Dec 2021 03:20:35 GMT  
		Size: 187.7 MB (187688794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b650ffc6e06ebc1cb11ab43326bd2e72987543cf6845f8a5c4f2a0fd555926`  
		Last Modified: Tue, 21 Dec 2021 22:35:12 GMT  
		Size: 6.9 KB (6874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e56d603fbb089a0bb9b4ad4a71cdaba1b36d8612bd2f8718096b9588c5487e7`  
		Last Modified: Tue, 21 Dec 2021 22:35:18 GMT  
		Size: 58.8 MB (58815373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a63157d0dd36188cae7e7a8b78e6f7b3b60146c830aa4c805ea9968d3944c4c`  
		Last Modified: Tue, 21 Dec 2021 22:35:12 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
