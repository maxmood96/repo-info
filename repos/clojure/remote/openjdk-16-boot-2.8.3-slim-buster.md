## `clojure:openjdk-16-boot-2.8.3-slim-buster`

```console
$ docker pull clojure@sha256:f6790e26aef31966989ea5645135bfbbf3e03724b991532d2925a14e491d3f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-16-boot-2.8.3-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:4b1ad37210c760e1f76defb6c53473a0a1539a5dfcbb7bdf1b8d2348e84be94f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274377839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d925af5036d473809dde691957ea89e58e9f53f390b30ab3f15a05f6be6e97ed`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 00:14:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 00:14:56 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 00:14:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Wed, 18 Nov 2020 00:14:57 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 00:14:59 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 01 Dec 2020 23:54:51 GMT
ENV JAVA_VERSION=16-ea+26
# Tue, 01 Dec 2020 23:55:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/26/GPL/openjdk-16-ea+26_linux-aarch64_bin.tar.gz; 			downloadSha256=1e2fefe414a16aceeae6816b4e48b426e79bb647927a44bbfe4d692156096e74; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/26/GPL/openjdk-16-ea+26_linux-x64_bin.tar.gz; 			downloadSha256=e74300f3f770122358d768d45e181d29c710e8d41bbc4ab8e492929f2867347c; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Dec 2020 23:55:21 GMT
CMD ["jshell"]
# Wed, 02 Dec 2020 00:33:21 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Dec 2020 00:33:22 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Dec 2020 00:33:22 GMT
WORKDIR /tmp
# Wed, 02 Dec 2020 00:33:27 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 02 Dec 2020 00:33:27 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Dec 2020 00:33:27 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Dec 2020 00:33:47 GMT
RUN boot
# Wed, 02 Dec 2020 00:33:47 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef17c1a944643971956760785cd2fdb1ae360b47af01d997bd7580f32b8b3512`  
		Last Modified: Wed, 18 Nov 2020 00:22:53 GMT  
		Size: 3.2 MB (3248467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f372ea5b91612afd4a4eedf6685a7aca438c668a5c19bc23dcb12519c861fb2`  
		Last Modified: Wed, 18 Nov 2020 00:22:51 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f3aefa653b4bee9ff46884a0e9cadb3f3c2dc1fdfd6694512decf0f9efcd39`  
		Last Modified: Wed, 02 Dec 2020 00:01:09 GMT  
		Size: 184.9 MB (184923919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182703c51fc662bcfabcc1bb1e90c60fd0f42443ac5c606c21979db4a290f18c`  
		Last Modified: Wed, 02 Dec 2020 00:36:48 GMT  
		Size: 279.6 KB (279574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc66926ad35951dbce824411f22ccd73be50e0fc808908c6a6b7fc1cd4d07585`  
		Last Modified: Wed, 02 Dec 2020 00:36:52 GMT  
		Size: 58.8 MB (58820184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
