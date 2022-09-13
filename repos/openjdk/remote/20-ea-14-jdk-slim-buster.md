## `openjdk:20-ea-14-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:197bc2f306c6e65b0282d1c4e0568803f67a514731634f23d0227d10284e166b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-14-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:d7844b0b85a451a470ea55df32eeccf373e57c29a7b56f2128dd9f80ece3a2e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227637267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d29ac6fc7c88deb4346181a3c16be0ec2e580a1dca4e8fe26b76ba4c3737cdd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:10 GMT
ADD file:baca493d7744d12304f6d9c7b6ec0800453a0ba02cbf4005ec35c7b921adf0c4 in / 
# Tue, 23 Aug 2022 00:21:10 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:30:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:30:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 23 Aug 2022 04:30:24 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Aug 2022 04:30:24 GMT
ENV LANG=C.UTF-8
# Mon, 12 Sep 2022 22:37:04 GMT
ENV JAVA_VERSION=20-ea+14
# Mon, 12 Sep 2022 22:37:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='ce9c99a0d70bf7c6548b68a33770a50d1273d5d5ea72522a1fe91ae6d3f22c1d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='4935236eb4e51be13ddfcc1ce717191128feb8ff9329676971ea54775261d9ff'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Sep 2022 22:37:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2238450926aa858e592e60bb5d68dd26eeab8a984eee45505ca89d2022e3b450`  
		Last Modified: Tue, 23 Aug 2022 00:25:43 GMT  
		Size: 27.1 MB (27138330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4bb2aa3cefa352eef3f71a4b1e2d70041ef3c1e9cf1b9802e5d43db17fcf35`  
		Last Modified: Tue, 23 Aug 2022 04:37:53 GMT  
		Size: 3.3 MB (3273368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94191a832b941fd54daad42db331c4d650c5b2e8748368346a048ffb3473fa9`  
		Last Modified: Mon, 12 Sep 2022 22:43:59 GMT  
		Size: 197.2 MB (197225569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-14-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:92f3e3be9b8b098218f4f9251ae0a6522c0eb138a22db53d7cc8c06e612286a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224569225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56cb865eec4fca0c81266b98966b49b0cc790ef27ff5efe5ab049623e6b55b9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:58 GMT
ADD file:4c5bca2d158b11314fb47a6d4b34239575621c2f00f92e77870f23aa02913fac in / 
# Tue, 23 Aug 2022 01:52:59 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 05:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 05:17:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Tue, 23 Aug 2022 05:17:34 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Aug 2022 05:17:35 GMT
ENV LANG=C.UTF-8
# Mon, 12 Sep 2022 23:06:01 GMT
ENV JAVA_VERSION=20-ea+14
# Mon, 12 Sep 2022 23:06:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='ce9c99a0d70bf7c6548b68a33770a50d1273d5d5ea72522a1fe91ae6d3f22c1d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='4935236eb4e51be13ddfcc1ce717191128feb8ff9329676971ea54775261d9ff'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Sep 2022 23:06:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a84b81edbdb892b3702892bbb01c240695b0b9d619fda43a9b951c9d2df1443c`  
		Last Modified: Tue, 23 Aug 2022 01:58:50 GMT  
		Size: 25.9 MB (25912515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356227960c8e171a8438469fe7c95bc6d10c5694b55ced0cb37aaaabaef7f2dc`  
		Last Modified: Tue, 23 Aug 2022 05:29:25 GMT  
		Size: 3.1 MB (3126086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f74f9b56358163a5b0ab444ca7e8b41b20878392508d6dfacb8c77f96c617bc`  
		Last Modified: Mon, 12 Sep 2022 23:16:51 GMT  
		Size: 195.5 MB (195530624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
