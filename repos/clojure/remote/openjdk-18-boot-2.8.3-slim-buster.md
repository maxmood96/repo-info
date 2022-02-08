## `clojure:openjdk-18-boot-2.8.3-slim-buster`

```console
$ docker pull clojure@sha256:95725b63d2844fb929090b2e6e6bb8bcc61b62fc116f2bad5fb2863ef5e685c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-2.8.3-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:32b636d288bb43eba44ec939fcf104f9a455c67ac7bc1279428667268b908d18
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278561359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c200e8e65ae5ca9cf6474c9b23079d718d911d716074f4390f958240f7e156a`
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
# Tue, 08 Feb 2022 03:46:28 GMT
ENV JAVA_VERSION=18-ea+34
# Tue, 08 Feb 2022 03:46:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='6811138655a3ede61c4e551db2fcc572bbf2bdfb6752777fcbf5d5b2a0affa6b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c60dee24ba0c181adce97eb72e4517212fe0a113ae048cb4f581e7326012812'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Feb 2022 03:46:45 GMT
CMD ["jshell"]
# Tue, 08 Feb 2022 06:07:34 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 08 Feb 2022 06:07:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 08 Feb 2022 06:07:34 GMT
WORKDIR /tmp
# Tue, 08 Feb 2022 06:07:39 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 08 Feb 2022 06:07:39 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 08 Feb 2022 06:07:40 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 08 Feb 2022 06:08:21 GMT
RUN boot
# Tue, 08 Feb 2022 06:08:22 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 08 Feb 2022 06:08:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 08 Feb 2022 06:08:22 GMT
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
	-	`sha256:e48ed738cc8312757bffe0c4c6e84438502dee0308eced4efd41e996c925d7c9`  
		Last Modified: Tue, 08 Feb 2022 04:01:22 GMT  
		Size: 189.0 MB (189036760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f3a18075e4677ac2da674f434b648b97d9fe19bdf7730b6cda2170ad0b18c5`  
		Last Modified: Tue, 08 Feb 2022 06:17:55 GMT  
		Size: 279.8 KB (279812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1c9c3113d2107bfd8ff60aaad241a2c23d5f7d8df13887eb01b8eaf4215f7a`  
		Last Modified: Tue, 08 Feb 2022 06:17:58 GMT  
		Size: 58.8 MB (58820962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9006d0ef9b061ab6f4992b289ff8029af19c192a7e9fac00b62c40bb80ed77ce`  
		Last Modified: Tue, 08 Feb 2022 06:17:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-2.8.3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0bd83c9aaeee95812f0c931b4abf595175a32322f9e05cd7e3563a943c83ba0d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275682899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0df5679e70ce6ded139a5a6cad0e159d11cfd1821a854eab15460363c430f4`
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
# Tue, 08 Feb 2022 06:27:57 GMT
ENV JAVA_VERSION=18-ea+34
# Tue, 08 Feb 2022 06:28:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='6811138655a3ede61c4e551db2fcc572bbf2bdfb6752777fcbf5d5b2a0affa6b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c60dee24ba0c181adce97eb72e4517212fe0a113ae048cb4f581e7326012812'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Feb 2022 06:28:12 GMT
CMD ["jshell"]
# Tue, 08 Feb 2022 09:26:13 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 08 Feb 2022 09:26:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 08 Feb 2022 09:26:15 GMT
WORKDIR /tmp
# Tue, 08 Feb 2022 09:26:25 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 08 Feb 2022 09:26:26 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 08 Feb 2022 09:26:27 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 08 Feb 2022 09:27:03 GMT
RUN boot
# Tue, 08 Feb 2022 09:27:04 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 08 Feb 2022 09:27:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 08 Feb 2022 09:27:05 GMT
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
	-	`sha256:59875ed1c00daa1d2e82ddd87223ae8aaa8fc9c7a72642f1bb322033bbfbb9fe`  
		Last Modified: Tue, 08 Feb 2022 08:28:27 GMT  
		Size: 187.8 MB (187756340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe07e91a4b5f93a5f5b5ed1e21c0e9f56e18dff6bb097b218f7e9fa55fc71fd`  
		Last Modified: Tue, 08 Feb 2022 09:38:48 GMT  
		Size: 67.6 KB (67556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557b4fbc5d6e2449112a16637ac8ca0e23924eb131588995d82c2e2ca85dda1e`  
		Last Modified: Tue, 08 Feb 2022 09:38:53 GMT  
		Size: 58.8 MB (58816522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08dab52338627d4644b5a40016179b083a29c26387b1843a888cdf7ac05ea8c`  
		Last Modified: Tue, 08 Feb 2022 09:38:48 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
