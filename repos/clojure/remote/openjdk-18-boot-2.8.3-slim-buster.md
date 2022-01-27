## `clojure:openjdk-18-boot-2.8.3-slim-buster`

```console
$ docker pull clojure@sha256:2690136e597df35120d675814e3a0368b0cf429557e4f4ba5690a77482665261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-2.8.3-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:1b0d3820378d3b3afa58a223d22fd93f4b1a99b6c12645f4469529e753761b54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278545836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bbcdc9163523f88e7e666b3614fc4c2b2ffb590689498f81afc7f69b5d132d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:19:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:21:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 09:21:10 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:21:11 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:21:11 GMT
ENV JAVA_VERSION=18-ea+31
# Wed, 26 Jan 2022 09:21:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/31/GPL/openjdk-18-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='d57d6a205ea5a0b891490b6d9e45315f719ba92123775c4e0e3e76464504f7fa'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/31/GPL/openjdk-18-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='668f2637087591644db894f1f03c5782bb491fd4452b0c736ab7f6e70f1eb036'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 26 Jan 2022 09:21:27 GMT
CMD ["jshell"]
# Thu, 27 Jan 2022 17:06:56 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 27 Jan 2022 17:06:56 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 27 Jan 2022 17:06:56 GMT
WORKDIR /tmp
# Thu, 27 Jan 2022 17:07:01 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 27 Jan 2022 17:07:02 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 27 Jan 2022 17:07:02 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 27 Jan 2022 17:07:26 GMT
RUN boot
# Thu, 27 Jan 2022 17:07:26 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 27 Jan 2022 17:07:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 27 Jan 2022 17:07:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa8d0f5eb646a53df0b867301afa43404e868c540fdf170240578844dfd0d6b`  
		Last Modified: Wed, 26 Jan 2022 09:43:10 GMT  
		Size: 3.3 MB (3269688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ace2dc38398daafd17b62b34a7bb2a78b97096331531522d95391c30a508a`  
		Last Modified: Wed, 26 Jan 2022 09:46:40 GMT  
		Size: 189.0 MB (189021416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159d947ad5fb27d5b84409539ff5256e69f0412c3aeec0af090035c10117fe18`  
		Last Modified: Thu, 27 Jan 2022 17:29:32 GMT  
		Size: 279.8 KB (279764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d97f90f68dac20f2e482b0a2fd7c11b3aa91b5bf808d9218149ac4c69d3157d`  
		Last Modified: Thu, 27 Jan 2022 17:29:35 GMT  
		Size: 58.8 MB (58820830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a924fbf85d285ae59cfb8bd8ab2aa842f52070e9530584affc5f15bd564c6b52`  
		Last Modified: Thu, 27 Jan 2022 17:29:31 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-2.8.3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:379a17793abdd78d08b67ab5d1937256ca292123f001693e286cfaed45249115
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275678621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4db6afb9d96234837143db07ad80c8025028c7c8c90053a1ec237f04aaa362`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 05:51:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:53:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 05:53:13 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 05:53:14 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 05:53:15 GMT
ENV JAVA_VERSION=18-ea+31
# Wed, 26 Jan 2022 05:53:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/31/GPL/openjdk-18-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='d57d6a205ea5a0b891490b6d9e45315f719ba92123775c4e0e3e76464504f7fa'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/31/GPL/openjdk-18-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='668f2637087591644db894f1f03c5782bb491fd4452b0c736ab7f6e70f1eb036'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 26 Jan 2022 05:53:35 GMT
CMD ["jshell"]
# Wed, 26 Jan 2022 21:24:44 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Jan 2022 21:24:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Jan 2022 21:24:46 GMT
WORKDIR /tmp
# Wed, 26 Jan 2022 21:24:51 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Jan 2022 21:24:52 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Jan 2022 21:24:53 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Jan 2022 21:25:07 GMT
RUN boot
# Wed, 26 Jan 2022 21:25:08 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 26 Jan 2022 21:25:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Jan 2022 21:25:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a5c9716b24a17043a5d8ede1303daffeaaa07ff0393fa14caed54f01154833`  
		Last Modified: Wed, 26 Jan 2022 06:14:50 GMT  
		Size: 3.1 MB (3118858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb130a9002dae95ffa39a11a09540a74920396c04ddea39d630c28cb1aeefd4`  
		Last Modified: Wed, 26 Jan 2022 06:18:34 GMT  
		Size: 187.8 MB (187753218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3effecb713626b6fd4929f41768de02e9b6482195b7816f67e574fd45849435e`  
		Last Modified: Wed, 26 Jan 2022 21:47:41 GMT  
		Size: 67.5 KB (67511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cebd7e67624d585665f68fa086f7815c48512229597a3feff6b283db3342c0`  
		Last Modified: Wed, 26 Jan 2022 21:47:48 GMT  
		Size: 58.8 MB (58815412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15a2692bbba42fbc389641c782ef7d9cacae78e95d9b5feab7c02fc4e77969c`  
		Last Modified: Wed, 26 Jan 2022 21:47:41 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
