## `clojure:openjdk-17-tools-deps-slim-buster`

```console
$ docker pull clojure@sha256:f94cb461e4f0abf3a127b275df7b108b5966e98353ad4bdc4e1bcc7760387933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-tools-deps-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:c54a0b6cc67b8c76260148179ec8e805f0cdf85d4a4135ff4911043402a3b69e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.4 MB (276412402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c63472d20e3c9cb04f998afb8275083fb855deef5b0f72a29f88c922de155f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 22:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 23:01:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 21 Dec 2021 23:01:29 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 23:01:29 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 23:01:29 GMT
ENV JAVA_VERSION=17.0.1
# Tue, 21 Dec 2021 23:01:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 23:01:46 GMT
CMD ["jshell"]
# Wed, 22 Dec 2021 13:39:53 GMT
ENV CLOJURE_VERSION=1.10.3.1040
# Wed, 22 Dec 2021 13:39:53 GMT
WORKDIR /tmp
# Wed, 22 Dec 2021 13:40:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "665e35e8d7dd0996edaba36220fd5048fee95f5155ec0426f628f18770239821 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 22 Dec 2021 13:40:11 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 22 Dec 2021 13:40:12 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 22 Dec 2021 13:40:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Dec 2021 13:40:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c983bcc370920d99695dc288c345343be841987206e4ce762a4e7599f28c96`  
		Last Modified: Tue, 21 Dec 2021 23:16:09 GMT  
		Size: 3.3 MB (3269567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2dd1934c7e37cb0dd1aa7edb2a85416feeb6ef8fb75c26de2a963b9e5c1efd`  
		Last Modified: Tue, 21 Dec 2021 23:22:31 GMT  
		Size: 187.5 MB (187548485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2701d8b6024f2e0d25c203ae666899cd5db39c7fafc5fb3596b9bdcf16163d1`  
		Last Modified: Wed, 22 Dec 2021 13:58:50 GMT  
		Size: 58.4 MB (58439596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6e95989054c68111869b7e78ac589c8f961b007c8577a0ee9082ba8154a114`  
		Last Modified: Wed, 22 Dec 2021 13:58:43 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dc18c425a1ef68b8c64a3a9172e6ddf0831d6635083012ec7ce38b415c5347`  
		Last Modified: Wed, 22 Dec 2021 13:58:43 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-tools-deps-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9db7a2dca6b6a490c3b5bad3bc9101c794ff999aa95b37a04c167372e4db94b5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.3 MB (273276536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eac98075a2a5de4ef60bd40b2df3a00e46612d75aa848f88577bc6b355543cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:58:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 21 Dec 2021 02:58:54 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:58:55 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 02:58:56 GMT
ENV JAVA_VERSION=17.0.1
# Tue, 21 Dec 2021 02:59:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 02:59:11 GMT
CMD ["jshell"]
# Tue, 21 Dec 2021 22:10:21 GMT
ENV CLOJURE_VERSION=1.10.3.1040
# Tue, 21 Dec 2021 22:10:21 GMT
WORKDIR /tmp
# Tue, 21 Dec 2021 22:10:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "665e35e8d7dd0996edaba36220fd5048fee95f5155ec0426f628f18770239821 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 21 Dec 2021 22:10:39 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 21 Dec 2021 22:10:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 21 Dec 2021 22:10:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Dec 2021 22:10:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c74145b5f237a66007b7c0d55f2ffe3d54c07bf5e09c19bebd4ec94b00005e`  
		Last Modified: Tue, 21 Dec 2021 03:17:41 GMT  
		Size: 3.1 MB (3118854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3f14d4fc26eea37b6d16d78a92f75e786a6efa868ec35267a831bfe148f318`  
		Last Modified: Tue, 21 Dec 2021 03:25:05 GMT  
		Size: 186.1 MB (186146523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c90d407b8e7c46a913fb4fdabe0277931e821c1fe7924f7c570382a6f75d8b`  
		Last Modified: Tue, 21 Dec 2021 22:33:42 GMT  
		Size: 58.1 MB (58086978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a92f765649961263eeb59db8dfab31f435b172bdc1c28ee16b3f60e39359cf0`  
		Last Modified: Tue, 21 Dec 2021 22:33:33 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8e44ddd3ca8c0a2b0d23246c18718b0e25b249f5458ac3cbfd503d0489d0d3`  
		Last Modified: Tue, 21 Dec 2021 22:33:33 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
