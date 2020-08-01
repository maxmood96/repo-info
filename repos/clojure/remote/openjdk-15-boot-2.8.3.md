## `clojure:openjdk-15-boot-2.8.3`

```console
$ docker pull clojure@sha256:9e0b99516b1162b09430fb05a3db238466f5918466c6ebab738d2d9550068a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-15-boot-2.8.3` - linux; amd64

```console
$ docker pull clojure@sha256:c2c3fcccc9609320150184f7c2d83685ae369a76bdc161a8a1c5bed79bf300bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285579293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91fc8ce6eba6516e480c594a1e21d25f4d8d19a34447254244209d10e43e335`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 22:35:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:35:24 GMT
ENV LANG=C.UTF-8
# Wed, 29 Jul 2020 01:26:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-15
# Wed, 29 Jul 2020 01:26:03 GMT
ENV PATH=/usr/local/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jul 2020 01:26:04 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 31 Jul 2020 22:24:10 GMT
ENV JAVA_VERSION=15-ea+34
# Fri, 31 Jul 2020 22:24:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/34/GPL/openjdk-15-ea+34_linux-aarch64_bin.tar.gz; 			downloadSha256=c3d653467f34723f6d2eeb8a1d9c0266f2222af6d07c18f58ca697e8ae2de1c2; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/34/GPL/openjdk-15-ea+34_linux-x64_bin.tar.gz; 			downloadSha256=359d74ed4010ef32ae32bb0665a7a62bc5d440aa17c382f22a6d103bf83589a5; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Fri, 31 Jul 2020 22:24:27 GMT
CMD ["jshell"]
# Fri, 31 Jul 2020 23:17:11 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 31 Jul 2020 23:17:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 31 Jul 2020 23:17:12 GMT
WORKDIR /tmp
# Fri, 31 Jul 2020 23:17:17 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 31 Jul 2020 23:17:17 GMT
ENV PATH=/usr/local/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 31 Jul 2020 23:17:17 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 31 Jul 2020 23:17:36 GMT
RUN boot
# Fri, 31 Jul 2020 23:17:36 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4e9b7780660af457791b3bbbd51d1d25c8d9681c1f7ebe5e3a59e0179cecd`  
		Last Modified: Wed, 22 Jul 2020 22:44:33 GMT  
		Size: 3.2 MB (3248441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb9bb9b7d051e91eee43856c2c35d5c940bc296414fd9a560794f48a17687e6`  
		Last Modified: Wed, 29 Jul 2020 01:34:09 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50cc4afa85fa870f97e9dd7f72e82affcebb5050b078d2df435e0d199158287`  
		Last Modified: Fri, 31 Jul 2020 22:28:40 GMT  
		Size: 196.1 MB (196132322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d17f707c45d7985b8ba812d297b5bca6fece56f80175759aef6995dd1047df9`  
		Last Modified: Fri, 31 Jul 2020 23:19:52 GMT  
		Size: 279.5 KB (279547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b020a9ce8211bb7df815c9a7969d62e7aec3ffe3700e48e6fc9963f9ba5dc8f3`  
		Last Modified: Fri, 31 Jul 2020 23:19:57 GMT  
		Size: 58.8 MB (58820230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
