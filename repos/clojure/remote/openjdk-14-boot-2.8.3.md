## `clojure:openjdk-14-boot-2.8.3`

```console
$ docker pull clojure@sha256:916b687b6c262c77a549be5b58bf2a2e6e97d5224876a8f4da27c5b6c1696754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-boot-2.8.3` - linux; amd64

```console
$ docker pull clojure@sha256:e248b95cf73462ef4ac9010aa77c8d1caf5afa65db51148b2e2a5b2dd28eede6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (288973091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf33aaa351c2cebf0a379710780aec464273d1a48080c1d3d0334b5bf18f44d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 21:00:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 21:00:03 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2020 21:01:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Fri, 15 May 2020 21:01:22 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 21:01:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 15 May 2020 21:01:24 GMT
ENV JAVA_VERSION=14.0.1
# Fri, 22 May 2020 01:24:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk14.0.1/664493ef4a6946b186ff29eb326336a2/7/GPL/openjdk-14.0.1_linux-x64_bin.tar.gz; 			downloadSha256=22ce248e0bd69f23028625bede9d1b3080935b68d011eaaf9e241f84d6b9c4cc; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Fri, 22 May 2020 01:24:39 GMT
CMD ["jshell"]
# Fri, 22 May 2020 02:07:15 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 22 May 2020 02:07:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 22 May 2020 02:07:16 GMT
WORKDIR /tmp
# Fri, 22 May 2020 02:07:21 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && echo "f717ef381f2863a4cad47bf0dcc61e923b3d2afb *boot.sh" | sha1sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get remove -y --purge wget && apt-get autoremove -y
# Fri, 22 May 2020 02:07:21 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 22 May 2020 02:07:21 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 22 May 2020 02:07:42 GMT
RUN boot
# Fri, 22 May 2020 02:07:43 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee19e84e8bd1140527176689c9c1a75f28c0462c0c714e549536452708cbfb64`  
		Last Modified: Fri, 15 May 2020 21:07:16 GMT  
		Size: 3.2 MB (3249166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e408fcb0b53eca4a06945015976a62523b7e8cf19378d876e61a492a1a7355`  
		Last Modified: Fri, 15 May 2020 21:08:33 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255ad6257ff4ca2539265a2ec1df682f50dafd91e80b1f18722dc08d1bd16feb`  
		Last Modified: Fri, 22 May 2020 01:28:57 GMT  
		Size: 199.5 MB (199525087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d60122f2c6a0bb244516ddb8b8ca31a2af792e70f2fca9a35e219a40ea2909`  
		Last Modified: Fri, 22 May 2020 02:09:37 GMT  
		Size: 279.6 KB (279623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c438b42964e43672b283b35bd6df3998976f75d4f8d34649445785a32320eb6`  
		Last Modified: Fri, 22 May 2020 02:09:39 GMT  
		Size: 58.8 MB (58820248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
