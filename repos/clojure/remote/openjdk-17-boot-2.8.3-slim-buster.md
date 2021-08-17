## `clojure:openjdk-17-boot-2.8.3-slim-buster`

```console
$ docker pull clojure@sha256:480f21fb4f378b96f9b8f1773b89541169bcbc64904bd31f3a008da0f1258bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-boot-2.8.3-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:0f07999d6fd66d46d0387904d787630d795298548eea59c73bb28a8ce5d60a41
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.0 MB (277038288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491b2713d57472d9db87bfa382a3dae23084c322c224aff2655f1a1bed7ff1f2`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 06:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 06:53:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 17 Aug 2021 06:53:40 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 06:53:40 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 06:53:40 GMT
ENV JAVA_VERSION=17
# Tue, 17 Aug 2021 06:53:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-x64_bin.tar.gz'; 			downloadSha256='aef49cc7aa606de2044302e757fa94c8e144818e93487081c4fd319ca858134b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-aarch64_bin.tar.gz'; 			downloadSha256='b8108a6b6c2579bd585281937cf09d401a5a971c59b9624e18abcf596b9caa22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 17 Aug 2021 06:53:54 GMT
CMD ["jshell"]
# Tue, 17 Aug 2021 18:36:58 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 17 Aug 2021 18:36:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 17 Aug 2021 18:36:59 GMT
WORKDIR /tmp
# Tue, 17 Aug 2021 18:37:06 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 17 Aug 2021 18:37:06 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Aug 2021 18:37:06 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 17 Aug 2021 18:37:36 GMT
RUN boot
# Tue, 17 Aug 2021 18:37:37 GMT
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
	-	`sha256:29579a70b04447ab452c6ca23752e1c6776c7a5a2a3a90aacffa487d201c93aa`  
		Last Modified: Tue, 17 Aug 2021 07:01:07 GMT  
		Size: 187.5 MB (187523198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541e4649a57aada9409e2ea043439d7463dc8f6d3d4517b503158111c179986d`  
		Last Modified: Tue, 17 Aug 2021 18:45:35 GMT  
		Size: 279.8 KB (279774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbd662dd409adea08067cef2b8f91e57d231628b1118ed8ec08261f816d65b2`  
		Last Modified: Tue, 17 Aug 2021 18:45:39 GMT  
		Size: 58.8 MB (58820563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-boot-2.8.3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:534068dacd9edfd7a2a277ad91e712889d1aeeb253167bd3b54fa5101aa5099b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274473443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b682016ae38ccde9ef5647d76b5800f49fa43f82b9ae8af679bac0df4d147dad`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 06:04:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 06:04:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 17 Aug 2021 06:04:46 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 06:04:46 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 06:04:46 GMT
ENV JAVA_VERSION=17
# Tue, 17 Aug 2021 06:05:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-x64_bin.tar.gz'; 			downloadSha256='aef49cc7aa606de2044302e757fa94c8e144818e93487081c4fd319ca858134b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-aarch64_bin.tar.gz'; 			downloadSha256='b8108a6b6c2579bd585281937cf09d401a5a971c59b9624e18abcf596b9caa22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 17 Aug 2021 06:05:04 GMT
CMD ["jshell"]
# Tue, 17 Aug 2021 15:13:01 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 17 Aug 2021 15:13:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 17 Aug 2021 15:13:01 GMT
WORKDIR /tmp
# Tue, 17 Aug 2021 15:13:11 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 17 Aug 2021 15:13:11 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Aug 2021 15:13:11 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 17 Aug 2021 15:13:32 GMT
RUN boot
# Tue, 17 Aug 2021 15:13:33 GMT
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
	-	`sha256:e938af235604b85cf613968df5e8114c58a97302658987ba6147755922390af1`  
		Last Modified: Tue, 17 Aug 2021 06:17:05 GMT  
		Size: 186.3 MB (186339312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6e77ed2f7eae11ddc81dc08af66a669bd630f140260dec638dbcfeec2604f2`  
		Last Modified: Tue, 17 Aug 2021 15:23:07 GMT  
		Size: 279.5 KB (279509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad47cef47f934d67604b0b3d061766313c63f6c45ffe21165ba517d8f2a1373`  
		Last Modified: Tue, 17 Aug 2021 15:23:11 GMT  
		Size: 58.8 MB (58820689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
