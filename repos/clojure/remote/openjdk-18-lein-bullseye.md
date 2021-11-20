## `clojure:openjdk-18-lein-bullseye`

```console
$ docker pull clojure@sha256:d9d01a2ee182b92213d0d1a61197030c1966a49e5e788fb0f6d23c3d90c507fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:76fec10226fa37c3f308437e9f29ed3f958837a6a626bff725e0b5ef75120663
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.4 MB (344374360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc775976015fb1b0e9fbdb0e37cf4d845b295c652deb30358c4f9a2e77f6bf2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:30 GMT
ADD file:5259fc086e8295ddbf02e48abef38e9bf93a183079d3631aa7a59306b7f2f9df in / 
# Wed, 17 Nov 2021 02:20:31 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:14:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:14:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 03:14:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:23:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 09:23:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 17 Nov 2021 09:23:37 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 09:23:38 GMT
ENV LANG=C.UTF-8
# Fri, 19 Nov 2021 23:44:35 GMT
ENV JAVA_VERSION=18-ea+24
# Fri, 19 Nov 2021 23:44:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/24/GPL/openjdk-18-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='be728d2d5f8887ffc348d5a3293938e069c24be47e082a0b61aea61ce328aa03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/24/GPL/openjdk-18-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='672dcbf3233da1ea245a7991fbeee867817d7024dc5c7e1b533240e642c27626'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 19 Nov 2021 23:44:46 GMT
CMD ["jshell"]
# Sat, 20 Nov 2021 01:34:57 GMT
ENV LEIN_VERSION=2.9.8
# Sat, 20 Nov 2021 01:34:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 20 Nov 2021 01:34:57 GMT
WORKDIR /tmp
# Sat, 20 Nov 2021 01:35:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg
# Sat, 20 Nov 2021 01:35:05 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 20 Nov 2021 01:35:05 GMT
ENV LEIN_ROOT=1
# Sat, 20 Nov 2021 01:35:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Sat, 20 Nov 2021 01:35:09 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:647acf3d48c2780e00cd27bb0984367415f270d78477ef9d5b238e6ebd5290da`  
		Last Modified: Wed, 17 Nov 2021 02:25:17 GMT  
		Size: 54.9 MB (54932774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02967ef003473d9adc6e20868d9d66af85b0871919bcec92419f65c974aa8ce`  
		Last Modified: Wed, 17 Nov 2021 03:23:07 GMT  
		Size: 5.2 MB (5153337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ad2231829e42e6f095971b5d2dc143d97db2d0870571ba4d29ecd599db62cb`  
		Last Modified: Wed, 17 Nov 2021 03:23:07 GMT  
		Size: 10.9 MB (10871856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5576ce26bf1df68da60eeb5162dccde1b69f865d2815aba8b2d29e7181aeb62b`  
		Last Modified: Wed, 17 Nov 2021 03:23:31 GMT  
		Size: 54.6 MB (54566324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b28f29762d60d8bac863b4a63f2ba6c54c9742be3d86e501038eaeefeae3213`  
		Last Modified: Wed, 17 Nov 2021 09:39:40 GMT  
		Size: 14.1 MB (14071679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e980a0f32945b6adddae7269229bac3f201266d6e295ca4869035e8a88d4d8e`  
		Last Modified: Fri, 19 Nov 2021 23:52:19 GMT  
		Size: 188.6 MB (188638474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06f4dca2791cd720f85a5101c2585d0a5a779f2779232e52b8443b0bb8febfd`  
		Last Modified: Sat, 20 Nov 2021 01:42:47 GMT  
		Size: 11.9 MB (11932746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f15973025a64d79f116a4f226f517c9272d62ed2534618dbf88eb8217a9294d`  
		Last Modified: Sat, 20 Nov 2021 01:42:47 GMT  
		Size: 4.2 MB (4207170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:df10cdab6478db17746f679aeaf44c5ae195208d36955dda17d7ee711117749a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.9 MB (342851732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172760fc7487054739a0f776d5ca9a17017ac2ffd8c2cc74bedeee20072977d6`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 17 Nov 2021 02:39:59 GMT
ADD file:eb667e18226da8a1ca5a41beacddc65cd1efec01c3d01e50845c5e89e91ea17c in / 
# Wed, 17 Nov 2021 02:40:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:26:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:26:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 13:27:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 21:53:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 21:53:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 17 Nov 2021 21:53:49 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 21:53:50 GMT
ENV LANG=C.UTF-8
# Fri, 19 Nov 2021 23:05:07 GMT
ENV JAVA_VERSION=18-ea+24
# Fri, 19 Nov 2021 23:05:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/24/GPL/openjdk-18-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='be728d2d5f8887ffc348d5a3293938e069c24be47e082a0b61aea61ce328aa03'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/24/GPL/openjdk-18-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='672dcbf3233da1ea245a7991fbeee867817d7024dc5c7e1b533240e642c27626'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 19 Nov 2021 23:05:19 GMT
CMD ["jshell"]
# Sat, 20 Nov 2021 03:47:04 GMT
ENV LEIN_VERSION=2.9.8
# Sat, 20 Nov 2021 03:47:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 20 Nov 2021 03:47:06 GMT
WORKDIR /tmp
# Sat, 20 Nov 2021 03:47:13 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg
# Sat, 20 Nov 2021 03:47:13 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 20 Nov 2021 03:47:14 GMT
ENV LEIN_ROOT=1
# Sat, 20 Nov 2021 03:47:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Sat, 20 Nov 2021 03:47:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ce18cd0ba11c2dfa8c1a2d2b325e1e019b14d4ae25ffdeffb0f9686c5496bf5c`  
		Last Modified: Wed, 17 Nov 2021 02:46:45 GMT  
		Size: 53.6 MB (53619024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f138a340a2373acc72dcc4ea9ef08bdf5648aabc5fe08f7e8d25222ca63b7ee`  
		Last Modified: Wed, 17 Nov 2021 13:36:26 GMT  
		Size: 4.9 MB (4937639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34c030205ccb8656e30a58f96bb1edbe7c59bf17f3329ae3c442ec897f2b270`  
		Last Modified: Wed, 17 Nov 2021 13:36:27 GMT  
		Size: 10.7 MB (10655878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7a1cfcc2070fbe1e702751d85f7074b93d142f6beb03ef66e9ba1c58bcc3e3`  
		Last Modified: Wed, 17 Nov 2021 13:36:49 GMT  
		Size: 54.7 MB (54669696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1144edcd33972cab010ca0b1b91cf2bdbf148b8d8934800283524afbaf8f917b`  
		Last Modified: Wed, 17 Nov 2021 22:08:47 GMT  
		Size: 15.5 MB (15524904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304304da65956fc0c7ffce8647af2b3db00b3f165a99234dd8da93b8a1acfe51`  
		Last Modified: Fri, 19 Nov 2021 23:18:08 GMT  
		Size: 187.5 MB (187544839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f1da757ffb9a4e3ac9564d3145fe3af2487b1f66d24474a03d52309d053e77`  
		Last Modified: Sat, 20 Nov 2021 03:56:55 GMT  
		Size: 11.7 MB (11692690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a911f67031d0ac2691306c3971b58a11a7ba4fb4a5d5af60199b0d7937ebb277`  
		Last Modified: Sat, 20 Nov 2021 03:56:55 GMT  
		Size: 4.2 MB (4207062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
