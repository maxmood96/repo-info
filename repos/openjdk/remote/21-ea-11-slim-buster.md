## `openjdk:21-ea-11-slim-buster`

```console
$ docker pull openjdk@sha256:34b0a831d2241cdf4bc939ce5208ac25f463a66558275d8eaa7f3b777c4d40d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-11-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:1f90ca13fea4693bec1012f37719e8cf644639c8828a2a40c3464f2e2faea4ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230157651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ee1cad514c7360c6b3eb33208b9a74b5cfaf646ae341f849749b1e6b44eeba`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:48 GMT
ADD file:6c5da7126f75c404a5d182eb6345153d6ea45be11da8be63a1bd355011412847 in / 
# Thu, 09 Feb 2023 03:20:48 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:48:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:48:19 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Thu, 09 Feb 2023 10:48:19 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 10:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2023 01:31:14 GMT
ENV JAVA_VERSION=21-ea+11
# Tue, 28 Feb 2023 01:31:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='44d5639ae3005e8f6a494ab42506f7fbbe7c366a17c7da792bcaf21a04f5be13'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4f1bfbab4042464ed8c0b6e462354db5e97320b7c74d257639fc4c05d3ce4827'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Feb 2023 01:31:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:29cd48154c03e9242f1ff4f9895cf886a344fb94c9b71029455e76e11214328f`  
		Last Modified: Thu, 09 Feb 2023 03:25:54 GMT  
		Size: 27.1 MB (27140531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2663dab68577a1981f0b3fc37a5c844efdc4fe97f8c1484772876d35aa3400c`  
		Last Modified: Thu, 09 Feb 2023 10:55:23 GMT  
		Size: 3.3 MB (3275972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d65a23878bffeded697d766540281a6f37a1cab6280fae169cc14c5ce54286`  
		Last Modified: Tue, 28 Feb 2023 01:36:18 GMT  
		Size: 199.7 MB (199741148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-11-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b09ed1c87497205bf6702d1ae4a46ee77b5eeea3e3f87e8ec348e563f23a9838
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227285269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32041f66b50bf802afca306e0627e41e0be07c14bd3c18589451d1d55125a63e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:56 GMT
ADD file:ab0ca1f1ee3db357c8de06fd63e3d5f0132541162438c121e99f29e6af190bfa in / 
# Wed, 01 Mar 2023 02:20:56 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:25:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Wed, 01 Mar 2023 05:25:13 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 05:25:13 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 05:25:13 GMT
ENV JAVA_VERSION=21-ea+11
# Wed, 01 Mar 2023 05:25:30 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='44d5639ae3005e8f6a494ab42506f7fbbe7c366a17c7da792bcaf21a04f5be13'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/11/GPL/openjdk-21-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='4f1bfbab4042464ed8c0b6e462354db5e97320b7c74d257639fc4c05d3ce4827'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 01 Mar 2023 05:25:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed22f951ea44cd39f81544a2f0bf196ad60d13c1428cea537535186be61818f7`  
		Last Modified: Wed, 01 Mar 2023 02:24:56 GMT  
		Size: 25.9 MB (25922699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d097c08e52f9ff771689670d39bd09c2779339cc38112e4f75380522d71e9cf`  
		Last Modified: Wed, 01 Mar 2023 05:29:40 GMT  
		Size: 3.1 MB (3131731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c7d86a540e7ba61087447c45dc5644433de37ea3b34b27be335b4299f45446`  
		Last Modified: Wed, 01 Mar 2023 05:29:52 GMT  
		Size: 198.2 MB (198230839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
