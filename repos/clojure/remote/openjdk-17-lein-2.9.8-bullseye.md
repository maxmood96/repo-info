## `clojure:openjdk-17-lein-2.9.8-bullseye`

```console
$ docker pull clojure@sha256:0d2c23a798b6db004b6e01c5bb878439762e7936f5638fb2fba255afece22342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-lein-2.9.8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d7f084eb2b77da9a78022521a24a6e644bfa2830863a22acccc7825aae06a8a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.0 MB (343001035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38498e5f66a41baa17e7bd020d8557978847010cf4b8d7e67938c1bab1ac5bec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:32 GMT
ADD file:c03517c5ddbed4053165bfdf984b27a006fb5f533ca80b5798232d96df221440 in / 
# Tue, 21 Dec 2021 01:22:32 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:51:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 01:51:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 01:52:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 22:57:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 23:00:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 21 Dec 2021 23:00:34 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 23:00:34 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 23:00:34 GMT
ENV JAVA_VERSION=17.0.1
# Tue, 21 Dec 2021 23:00:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 23:00:46 GMT
CMD ["jshell"]
# Wed, 22 Dec 2021 13:47:41 GMT
ENV LEIN_VERSION=2.9.8
# Wed, 22 Dec 2021 13:47:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Dec 2021 13:47:41 GMT
WORKDIR /tmp
# Wed, 22 Dec 2021 13:47:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg
# Wed, 22 Dec 2021 13:47:48 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Dec 2021 13:47:48 GMT
ENV LEIN_ROOT=1
# Wed, 22 Dec 2021 13:47:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Wed, 22 Dec 2021 13:47:53 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 22 Dec 2021 13:47:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Dec 2021 13:47:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e29546d541cdbd309281d21a73a9d1db78665c1b95b74f32b009e0b77a6e1e3`  
		Last Modified: Tue, 21 Dec 2021 01:27:20 GMT  
		Size: 54.9 MB (54919034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b829c73b52b92b97d5c07a54fb0f3e921995a296c714b53a32ae67d19231fcd`  
		Last Modified: Tue, 21 Dec 2021 02:01:26 GMT  
		Size: 5.2 MB (5152816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5b7ae361722f070eca53f35823ed21baa85d61d5d95cd5a95ab53d740cdd56`  
		Last Modified: Tue, 21 Dec 2021 02:01:26 GMT  
		Size: 10.9 MB (10871868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6494e4811622b31c027ccac322ca463937fd805f569a93e6f15c01aade718793`  
		Last Modified: Tue, 21 Dec 2021 02:01:49 GMT  
		Size: 54.6 MB (54566215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b102718924c67af431330a4eae288cb9c4236caa5c79864e71c8aa3be8808138`  
		Last Modified: Tue, 21 Dec 2021 23:14:04 GMT  
		Size: 14.1 MB (14071715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f19edfe1543543670b1a07d5a169d5e0979b06f1b06c6ec8d475e064a61ac6`  
		Last Modified: Tue, 21 Dec 2021 23:20:02 GMT  
		Size: 187.3 MB (187279035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32f33e1a8b0d62497abadd7931403453d0f3e57a9e9304df1e09cd03863b5c9`  
		Last Modified: Wed, 22 Dec 2021 14:04:55 GMT  
		Size: 11.9 MB (11932697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3820ec9166c9b7d7522c022ceea70f2fd92c4ca6bb61775c712be790b45849`  
		Last Modified: Wed, 22 Dec 2021 14:04:54 GMT  
		Size: 4.2 MB (4207249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d35dea31c5f92db68b5ab9df9d35d40070e1f9bdcf78e0649487e24f18cbfa7`  
		Last Modified: Wed, 22 Dec 2021 14:04:54 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-lein-2.9.8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:03f732554faf3a274d4531dbeed18ee8cbceb7ca8cecf083954d9e3446c24347
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.6 MB (341581493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f56f38fc1636a3cb3af44a6d400f0db4f003675fe8249b850618974d4fcf1b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:08 GMT
ADD file:9d88e8701cd12aaee44dac3542cc3e4586f6382541afff76e56e8fb5275387d3 in / 
# Tue, 21 Dec 2021 01:42:09 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:12:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:52:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:57:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 21 Dec 2021 02:57:34 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:57:35 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 02:57:36 GMT
ENV JAVA_VERSION=17.0.1
# Tue, 21 Dec 2021 02:57:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 02:57:49 GMT
CMD ["jshell"]
# Tue, 21 Dec 2021 22:19:14 GMT
ENV LEIN_VERSION=2.9.8
# Tue, 21 Dec 2021 22:19:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 21 Dec 2021 22:19:15 GMT
WORKDIR /tmp
# Tue, 21 Dec 2021 22:19:21 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg
# Tue, 21 Dec 2021 22:19:22 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Dec 2021 22:19:23 GMT
ENV LEIN_ROOT=1
# Tue, 21 Dec 2021 22:19:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 21 Dec 2021 22:19:29 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 21 Dec 2021 22:19:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Dec 2021 22:19:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:94a23d3cb5be24659b25f17537307e7f568d665244f6a383c1c6e51e31080749`  
		Last Modified: Tue, 21 Dec 2021 01:48:23 GMT  
		Size: 53.6 MB (53604608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9d381bd1e98fa8759f80ff42db63c8fce4ac9407b2e7c8e0f031ed9f96432b`  
		Last Modified: Tue, 21 Dec 2021 02:22:29 GMT  
		Size: 5.1 MB (5141526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9c5b49b9db3dd2553e8ae6c2081b77274ec0a8b1f9903b0e5ac83900642098`  
		Last Modified: Tue, 21 Dec 2021 02:22:30 GMT  
		Size: 10.7 MB (10655891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841dd868500b6685b6cda93c97ea76e817b427d7a10bf73e9d03356fac199ffd`  
		Last Modified: Tue, 21 Dec 2021 02:22:52 GMT  
		Size: 54.7 MB (54668906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6575128af71feb3eba6809b36717cd9a918ad4434aa65d121f228313ad6c2fc1`  
		Last Modified: Tue, 21 Dec 2021 03:15:17 GMT  
		Size: 15.5 MB (15525097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c385b89db90b7b7b97633cfae8fdf1241537b93a91b615c8ac557f6a6015b1e`  
		Last Modified: Tue, 21 Dec 2021 03:22:16 GMT  
		Size: 186.1 MB (186085317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24546c4c26c17e2e82b1c9e5d08cce1af45d79bca66ec287aedb0043c4779b41`  
		Last Modified: Tue, 21 Dec 2021 22:40:52 GMT  
		Size: 11.7 MB (11692671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3aaa2152362da54fb6b6ffec114548992e40ecc9f682527944b0f4cf30a18c`  
		Last Modified: Tue, 21 Dec 2021 22:40:52 GMT  
		Size: 4.2 MB (4207069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac707aed7d3d7ea7903e0e056b2eb1ab17f97e509b29fe22e9baf9bbb5946b10`  
		Last Modified: Tue, 21 Dec 2021 22:40:51 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
