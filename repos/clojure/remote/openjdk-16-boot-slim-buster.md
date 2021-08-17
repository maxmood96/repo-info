## `clojure:openjdk-16-boot-slim-buster`

```console
$ docker pull clojure@sha256:3ec2c2251ace12b6dc53ad50a5e39f9f0dc133bcce9bc7133edfe1c3693d3869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-16-boot-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:80fa99fe74065a0114f94c34a95f429f60d08f181678dabde6d8cb30ce7c5bf1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274704597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f7d63a02f53d351c6b54cab1ba05116b26d84d34cddc99df3698358e950b82`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 06:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 06:54:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Tue, 17 Aug 2021 06:54:11 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 06:54:11 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 06:54:11 GMT
ENV JAVA_VERSION=16.0.2
# Tue, 17 Aug 2021 06:54:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.2/d4a915d82b4c4fbb9bde534da945d746/7/GPL/openjdk-16.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='6c714ded7d881ca54970ec949e283f43d673a142fda1de79b646ddd619da9c0c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.2/d4a915d82b4c4fbb9bde534da945d746/7/GPL/openjdk-16.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ffb9c7748334945d9056b3324de3f797d906fce4dad86beea955153aa1e28fe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 17 Aug 2021 06:54:26 GMT
CMD ["jshell"]
# Tue, 17 Aug 2021 18:35:02 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 17 Aug 2021 18:35:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 17 Aug 2021 18:35:02 GMT
WORKDIR /tmp
# Tue, 17 Aug 2021 18:35:10 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 17 Aug 2021 18:35:10 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Aug 2021 18:35:10 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 17 Aug 2021 18:35:40 GMT
RUN boot
# Tue, 17 Aug 2021 18:35:40 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427b7134c0c7b2e1d9cc703e20a84b850cbbf34ef654cfa0db710678a99da78b`  
		Last Modified: Tue, 17 Aug 2021 07:00:00 GMT  
		Size: 3.3 MB (3268768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ad83747fb7044c2d6fcded5230f47d13e824250a8f11b72b2b24989f2f1bf5`  
		Last Modified: Tue, 17 Aug 2021 07:01:53 GMT  
		Size: 185.2 MB (185189599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1170fe7cf317d67900149d689790afc2ce30f8623b90d00ef260835f40eb510`  
		Last Modified: Tue, 17 Aug 2021 18:44:24 GMT  
		Size: 279.7 KB (279701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89972fcdcd07cceac577c4ba4c659a57238df0b3b1ee122accac770276e0e753`  
		Last Modified: Tue, 17 Aug 2021 18:44:29 GMT  
		Size: 58.8 MB (58820544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-16-boot-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ecfc225597d0e34bdf022b837c643e407e0cbc9db1d6affb524fb6132a1e91c3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267698493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134657ff3ab16439f9c015db2cf86bc4e66e62b46ed979ef08363a7bca7b4f0a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 06:04:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 06:05:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Tue, 17 Aug 2021 06:05:42 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 06:05:42 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 06:05:42 GMT
ENV JAVA_VERSION=16.0.2
# Tue, 17 Aug 2021 06:05:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.2/d4a915d82b4c4fbb9bde534da945d746/7/GPL/openjdk-16.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='6c714ded7d881ca54970ec949e283f43d673a142fda1de79b646ddd619da9c0c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.2/d4a915d82b4c4fbb9bde534da945d746/7/GPL/openjdk-16.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ffb9c7748334945d9056b3324de3f797d906fce4dad86beea955153aa1e28fe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 17 Aug 2021 06:06:00 GMT
CMD ["jshell"]
# Tue, 17 Aug 2021 15:11:19 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 17 Aug 2021 15:11:20 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 17 Aug 2021 15:11:20 GMT
WORKDIR /tmp
# Tue, 17 Aug 2021 15:11:30 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 17 Aug 2021 15:11:30 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Aug 2021 15:11:30 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 17 Aug 2021 15:11:54 GMT
RUN boot
# Tue, 17 Aug 2021 15:11:54 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82a27af984eefbe6b82ccb775aead56e92f82cf16d079218087ebe132125cf5`  
		Last Modified: Tue, 17 Aug 2021 06:15:41 GMT  
		Size: 3.1 MB (3118861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de3aa2062429ebafd7dc6147fa3cdcf33ede564c40d101f2b8982dde3f1f9b1`  
		Last Modified: Tue, 17 Aug 2021 06:18:05 GMT  
		Size: 179.6 MB (179564525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82d10a65121fa21c0b40e4c17051f7f88ae7b8a1f2f4ba585725c4306484b20`  
		Last Modified: Tue, 17 Aug 2021 15:21:49 GMT  
		Size: 279.5 KB (279533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42677a17cdca9305341c5b20e3553d7cd3f6f4cccfa68d90e084a8040baba9f5`  
		Last Modified: Tue, 17 Aug 2021 15:21:53 GMT  
		Size: 58.8 MB (58820502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
