## `clojure:openjdk-18-tools-deps-slim-bullseye`

```console
$ docker pull clojure@sha256:27f9210512f2e8849ca2ead478dd8327bd97876a72cb72ed254ce7cb30a5dfa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-tools-deps-slim-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:000f578d4d01a558c5502966d9d5026ca35337272c209500552abd0c388f89a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278736530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4c984c4315c7d7f3acb38a2f4d4c40563742c41ff999378e42e55849f52637`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 22:57:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 22:59:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 21 Dec 2021 22:59:22 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 22:59:22 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 22:59:22 GMT
ENV JAVA_VERSION=18-ea+28
# Tue, 21 Dec 2021 22:59:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='7e5f0e54c799f8c155a934e61d88f4fef3a70a641c1636c925158622c7bd9341'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='e29aa39763ebcfe5f037cc4fe47c6b9eb34cbe482f6ea57e93de89070255e22b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 22:59:37 GMT
CMD ["jshell"]
# Wed, 22 Dec 2021 13:51:07 GMT
ENV CLOJURE_VERSION=1.10.3.1040
# Wed, 22 Dec 2021 13:51:07 GMT
WORKDIR /tmp
# Wed, 22 Dec 2021 13:51:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "665e35e8d7dd0996edaba36220fd5048fee95f5155ec0426f628f18770239821 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 22 Dec 2021 13:51:24 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 22 Dec 2021 13:51:24 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 22 Dec 2021 13:51:25 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Dec 2021 13:51:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbde5250315969db657b55bd8b2f5507fb659c0cf7f135edc84b684ffeab44a`  
		Last Modified: Tue, 21 Dec 2021 23:14:38 GMT  
		Size: 1.6 MB (1582039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61815ebdef528175531edb6014c6c3fb724e1fcd7413613f6dabe1fa530e311`  
		Last Modified: Tue, 21 Dec 2021 23:17:43 GMT  
		Size: 189.0 MB (189008775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c716e2c81a983ec16ffb65a1d57d2f298986ed4cc3dd15963c9ea77b26878b`  
		Last Modified: Wed, 22 Dec 2021 14:07:58 GMT  
		Size: 56.8 MB (56787065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b4e33b8fefa358039d9a8ffa4ea6e1c9e2809ed1eb1a431fa965beea166b38`  
		Last Modified: Wed, 22 Dec 2021 14:07:50 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8717497d1d3b6582aedf63ad029dd8b448825c78abfd7000b22cacd9afa5683c`  
		Last Modified: Wed, 22 Dec 2021 14:07:50 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-tools-deps-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9549715709ad5bec833d90bc8896841adf84294b3b8e6ef211b2979b98a688c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276052221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d1b57193719f5fdab53bee9980c71f3d377e4f376b9ee752b1fcb039be9fe1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:23 GMT
ADD file:986f91febed4aa8e2072081ff8419d52ba2060510822e717086d3b3d9469e4d7 in / 
# Tue, 21 Dec 2021 01:42:24 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:53:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:55:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 21 Dec 2021 02:55:51 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:55:52 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 02:55:53 GMT
ENV JAVA_VERSION=18-ea+28
# Tue, 21 Dec 2021 02:56:08 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='7e5f0e54c799f8c155a934e61d88f4fef3a70a641c1636c925158622c7bd9341'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='e29aa39763ebcfe5f037cc4fe47c6b9eb34cbe482f6ea57e93de89070255e22b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 02:56:09 GMT
CMD ["jshell"]
# Tue, 21 Dec 2021 22:22:51 GMT
ENV CLOJURE_VERSION=1.10.3.1040
# Tue, 21 Dec 2021 22:22:52 GMT
WORKDIR /tmp
# Tue, 21 Dec 2021 22:23:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "665e35e8d7dd0996edaba36220fd5048fee95f5155ec0426f628f18770239821 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 21 Dec 2021 22:23:10 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 21 Dec 2021 22:23:11 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 21 Dec 2021 22:23:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Dec 2021 22:23:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:927a35006d93ea08499b57046904046d7926cd76fb17be193e3e74f56d634a08`  
		Last Modified: Tue, 21 Dec 2021 01:48:54 GMT  
		Size: 30.0 MB (30043793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3380d13c6c3ddd0cc31ece5496ad1481500cb07b7feb31c81bc907a9a1ad71`  
		Last Modified: Tue, 21 Dec 2021 03:15:59 GMT  
		Size: 1.6 MB (1565954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53693c9efeb22abeaa3e69fa7f13fe2111db369cce1589baad869398b5d11189`  
		Last Modified: Tue, 21 Dec 2021 03:19:39 GMT  
		Size: 187.7 MB (187729842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a6010c568488cdc558627a06fcedb3985f4681eaef8ecae0e1203b0fdb950f`  
		Last Modified: Tue, 21 Dec 2021 22:44:37 GMT  
		Size: 56.7 MB (56711606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c030889807cf0fceb816752481341fab8788deba7a96f16ef443c022313dadd5`  
		Last Modified: Tue, 21 Dec 2021 22:44:29 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce706529fd680286feb3b22941a6385db0dba303e43f4914c25f1a6458ad0074`  
		Last Modified: Tue, 21 Dec 2021 22:44:29 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
