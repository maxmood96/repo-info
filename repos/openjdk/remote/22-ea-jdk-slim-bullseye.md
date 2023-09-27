## `openjdk:22-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:c28a88ab242d05e8e9e8851e9d7173291e73a77e62ae6ea849b637b6ee91ba66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:b98e9bc3b808528dcaa864e9420dd168c75cc15482ed61561797478652e60efc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238430926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6161a39d62b833f78920e66f25330e0c7574c84c7588e9169479d97398d8d50d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 06:16:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 06:16:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 20 Sep 2023 06:16:45 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 06:16:45 GMT
ENV LANG=C.UTF-8
# Wed, 27 Sep 2023 00:42:59 GMT
ENV JAVA_VERSION=22-ea+16
# Wed, 27 Sep 2023 00:43:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/16/GPL/openjdk-22-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='4bea3daa0a5dc0234dad8381ffb3322598e7f88d6190b21ebef4d01327b266ab'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/16/GPL/openjdk-22-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='34b3154d77f547b0b75d3bd2d534b38af115c75e2b395f1994c9adf923a8f3c3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 27 Sep 2023 00:43:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6450b6ea4fa89bead82ea896a53e3dfc6ad66d97a14a9f56241d71c097c8e0e1`  
		Last Modified: Wed, 20 Sep 2023 06:19:33 GMT  
		Size: 1.6 MB (1582466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ac0c4c2be9c56f067bc7aa0a26b8c127f4f34fcc52a0ca1328ecbb77b57533`  
		Last Modified: Wed, 27 Sep 2023 00:47:35 GMT  
		Size: 205.4 MB (205430749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a314dd0a89ebe988d65a9635fa068bd436b6bc47c5d94041d926074473db1d82
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235384459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f892dc91441dcc5142c8cb6ff27ec56133a8326d86fa82bca069cb51af0130`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:58:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 20 Sep 2023 17:58:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 17:58:12 GMT
ENV LANG=C.UTF-8
# Wed, 27 Sep 2023 01:10:18 GMT
ENV JAVA_VERSION=22-ea+16
# Wed, 27 Sep 2023 01:10:30 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/16/GPL/openjdk-22-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='4bea3daa0a5dc0234dad8381ffb3322598e7f88d6190b21ebef4d01327b266ab'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/16/GPL/openjdk-22-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='34b3154d77f547b0b75d3bd2d534b38af115c75e2b395f1994c9adf923a8f3c3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 27 Sep 2023 01:10:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3cb87782f1498c5adbce22d6724eb58d2770ffdc0c184aa7d27ca35e61138f`  
		Last Modified: Wed, 20 Sep 2023 18:02:07 GMT  
		Size: 1.6 MB (1566445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbfaaf1f8a7a19daddb929a69ebbb572152099aef15b75f7c30a2d933a241cc5`  
		Last Modified: Wed, 27 Sep 2023 01:14:19 GMT  
		Size: 203.8 MB (203755145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
