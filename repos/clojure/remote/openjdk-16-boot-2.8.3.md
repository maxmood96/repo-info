## `clojure:openjdk-16-boot-2.8.3`

```console
$ docker pull clojure@sha256:1435d33097a7e448d0ecb2cac871c0671b65b42c67ce67dd2908e82d8e3a2d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-16-boot-2.8.3` - linux; amd64

```console
$ docker pull clojure@sha256:6d69cbc56312e72df228312fc1ce448cd7f88272a79761c5cd17cd37bf42aecb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288821869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f34f01dabe9ef3dda4fd4823396eda2cd54ff1d6601e4c0e938334dfddca547`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 08:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 08:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 08:58:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Tue, 13 Oct 2020 08:58:54 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Oct 2020 08:58:55 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 22 Oct 2020 23:35:32 GMT
ENV JAVA_VERSION=16-ea+21
# Thu, 22 Oct 2020 23:35:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/21/GPL/openjdk-16-ea+21_linux-aarch64_bin.tar.gz; 			downloadSha256=bee09458526a8c10a40f3d4e5bf6c384b1bbc6f9002997d2f4c0d8c090cca1f8; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/21/GPL/openjdk-16-ea+21_linux-x64_bin.tar.gz; 			downloadSha256=3294d805c6125a6dd55a387f82f74df0c9fc0bce06934061fb3ff2dd42075b33; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 22 Oct 2020 23:35:53 GMT
CMD ["jshell"]
# Fri, 23 Oct 2020 00:04:29 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 23 Oct 2020 00:04:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 23 Oct 2020 00:04:30 GMT
WORKDIR /tmp
# Fri, 23 Oct 2020 00:04:35 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 23 Oct 2020 00:04:35 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 23 Oct 2020 00:04:35 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 23 Oct 2020 00:04:53 GMT
RUN boot
# Fri, 23 Oct 2020 00:04:53 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00028440d132be6f9dd59a787bc5d1372d575a539c19954651757f12912f2e65`  
		Last Modified: Tue, 13 Oct 2020 09:08:08 GMT  
		Size: 3.2 MB (3248445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d3f9016801bc943373bbb1397fe32a0219af3d56f3a8361ffae543191883ce`  
		Last Modified: Tue, 13 Oct 2020 09:08:07 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d71dd9e7d86f921ef2f6da833c80f1eca8229ff704ad697413cc4d5dc502ce0`  
		Last Modified: Thu, 22 Oct 2020 23:41:25 GMT  
		Size: 199.4 MB (199381352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faafdad191be3d7f0aabf1ce0699cfb9acc7289dfc0f3aa10806bcde0aa5bda4`  
		Last Modified: Fri, 23 Oct 2020 00:09:13 GMT  
		Size: 279.5 KB (279537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32f4c78d6de04274c5251b6f1a2eabe62be7ee7f78d0ef9eb7334098340bab0`  
		Last Modified: Fri, 23 Oct 2020 00:09:17 GMT  
		Size: 58.8 MB (58820096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
