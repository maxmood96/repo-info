## `clojure:openjdk-18-boot-2.8.3-slim-bullseye`

```console
$ docker pull clojure@sha256:e8bd52eb5f92dbf5d65c5f9def834960c605267697ca621d738ac1ba275751dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-2.8.3-slim-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6923e1bf7c95856e6be58193565fe248c23bc3f9f29e2cf03890404b86ce82ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281083813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62c69d993d26b4c827a988bbafe7b8f9c70255f307a12b1affbc0108d4fd78f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:20:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 09:20:29 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:20:29 GMT
ENV LANG=C.UTF-8
# Tue, 08 Feb 2022 03:45:51 GMT
ENV JAVA_VERSION=18-ea+34
# Tue, 08 Feb 2022 03:46:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='6811138655a3ede61c4e551db2fcc572bbf2bdfb6752777fcbf5d5b2a0affa6b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c60dee24ba0c181adce97eb72e4517212fe0a113ae048cb4f581e7326012812'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Feb 2022 03:46:07 GMT
CMD ["jshell"]
# Tue, 08 Feb 2022 06:11:00 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 08 Feb 2022 06:11:00 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 08 Feb 2022 06:11:01 GMT
WORKDIR /tmp
# Tue, 08 Feb 2022 06:11:05 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 08 Feb 2022 06:11:05 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 08 Feb 2022 06:11:05 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 08 Feb 2022 06:11:28 GMT
RUN boot
# Tue, 08 Feb 2022 06:11:28 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 08 Feb 2022 06:11:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 08 Feb 2022 06:11:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91b8877fa6956069d8fc9b8695ff61c45112cf8db300a45a823ee2ef3981f3f`  
		Last Modified: Tue, 08 Feb 2022 03:59:57 GMT  
		Size: 189.0 MB (189031536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07d58d5f6f8b240818cea017d7986921ca116e8404e0b537e7f08e80307bcef`  
		Last Modified: Tue, 08 Feb 2022 06:19:56 GMT  
		Size: 283.1 KB (283105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173fb479e9b711fc627a1bf52772440d1b97114b195e86db8acd59ed7aeda240`  
		Last Modified: Tue, 08 Feb 2022 06:20:00 GMT  
		Size: 58.8 MB (58820458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae4a65f100211c9bae4379c48a665a11ea32c23159e3073faef82c22abfb76a`  
		Last Modified: Tue, 08 Feb 2022 06:19:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-2.8.3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cc3ea334ce31ac9cd1629bee0540bf6e7590ba8edd96cdee01c5a9a68c301a74
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278256416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea22931ed7332b08468b1dfe0694a4a2025c213fe392c43fbcb5689e556345a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:31 GMT
ADD file:0ec6f47a8857bf8e6cef71ed8f864be7ce1790ff6ed04fd4201e7dbde4728d3a in / 
# Wed, 26 Jan 2022 01:42:31 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 05:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:52:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 05:52:14 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 05:52:15 GMT
ENV LANG=C.UTF-8
# Tue, 08 Feb 2022 06:27:12 GMT
ENV JAVA_VERSION=18-ea+34
# Tue, 08 Feb 2022 06:27:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='6811138655a3ede61c4e551db2fcc572bbf2bdfb6752777fcbf5d5b2a0affa6b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c60dee24ba0c181adce97eb72e4517212fe0a113ae048cb4f581e7326012812'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Feb 2022 06:27:27 GMT
CMD ["jshell"]
# Tue, 08 Feb 2022 09:31:07 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 08 Feb 2022 09:31:07 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 08 Feb 2022 09:31:08 GMT
WORKDIR /tmp
# Tue, 08 Feb 2022 09:31:13 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 08 Feb 2022 09:31:14 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 08 Feb 2022 09:31:15 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 08 Feb 2022 09:31:29 GMT
RUN boot
# Tue, 08 Feb 2022 09:31:30 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 08 Feb 2022 09:31:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 08 Feb 2022 09:31:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8998bd30e6a1204d13403045766edbe14f941b52087465f5d140ab63c8b113bf`  
		Last Modified: Wed, 26 Jan 2022 01:49:04 GMT  
		Size: 30.1 MB (30056774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abf67e3e34eccefabf68f15c7d753f1a4c8e241beb1818f97e276186d54124e`  
		Last Modified: Wed, 26 Jan 2022 06:13:02 GMT  
		Size: 1.6 MB (1565889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30ad345fa4797843c974b323f23703434d9a83c124d5556c02e70a91e6f26bb`  
		Last Modified: Tue, 08 Feb 2022 08:26:49 GMT  
		Size: 187.8 MB (187750552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8199c7a834e6d660152c9b8dc9912f7568970bdf52fe5e3f66356a77534491a7`  
		Last Modified: Tue, 08 Feb 2022 09:41:35 GMT  
		Size: 67.2 KB (67213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f339225f601fb2163af8d88ad59466277bd98d9eed5500d168e50c4beac7dd`  
		Last Modified: Tue, 08 Feb 2022 09:41:40 GMT  
		Size: 58.8 MB (58815583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1564992e1aab12c3d2ed6eb29bcbfb014176d8893f47f0519a3f00b2b487b1`  
		Last Modified: Tue, 08 Feb 2022 09:41:35 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
