## `clojure:openjdk-18`

```console
$ docker pull clojure@sha256:cddaf8c8daedca20fab02f45e3fdabf5754c1022f008757af0a8020d3effb725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18` - linux; amd64

```console
$ docker pull clojure@sha256:4365d9fd9bbbfd0a42c69f4ed06100d70f61f109bf4c748670a313ec473c8d3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278683057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b27a2cc0c5bb30b89f34ae5d84a8a856d500f931b50c7b3cdc823d71481f32`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:29:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Thu, 02 Dec 2021 11:29:27 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:29:27 GMT
ENV LANG=C.UTF-8
# Fri, 03 Dec 2021 23:47:13 GMT
ENV JAVA_VERSION=18-ea+26
# Fri, 03 Dec 2021 23:47:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/26/GPL/openjdk-18-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='fdf145c2819ef28edee67b7a6605bee89aefc505a1abea1686bec03fcba87c70'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/26/GPL/openjdk-18-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='14e35be6e99a093bd4d5666bd4d557ebb94ab9e03eab9e9ae0eb69fc7b3e662b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 03 Dec 2021 23:47:28 GMT
CMD ["jshell"]
# Sat, 04 Dec 2021 00:19:09 GMT
ENV CLOJURE_VERSION=1.10.3.1040
# Sat, 04 Dec 2021 00:19:09 GMT
WORKDIR /tmp
# Sat, 04 Dec 2021 00:19:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "665e35e8d7dd0996edaba36220fd5048fee95f5155ec0426f628f18770239821 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 04 Dec 2021 00:19:28 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 04 Dec 2021 00:19:28 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 04 Dec 2021 00:19:28 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Dec 2021 00:19:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9f5b9b70c2f137dc70e816256e7a568a084d066e7c34c028d30a6a45438685`  
		Last Modified: Thu, 02 Dec 2021 11:47:20 GMT  
		Size: 1.6 MB (1582045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d12dc13837c7f8f2dd4d1ad77ef51bd19b6671bd7da7a4a64ab05fc78ed329`  
		Last Modified: Fri, 03 Dec 2021 23:55:17 GMT  
		Size: 188.9 MB (188945751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ee597966b5e5447bff99a85f36f7cfa320174c2863e76125f0fdda0b408cc6`  
		Last Modified: Sat, 04 Dec 2021 00:25:52 GMT  
		Size: 56.8 MB (56784012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bde59bb571677c3182a819bf8dd5d295d37a9212fd70a585fbbeb5bbd02546`  
		Last Modified: Sat, 04 Dec 2021 00:25:45 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbd0b217c1138d49130cb65482016e00cb4d15cd18eb0a7831842f5e1a0c7d9`  
		Last Modified: Sat, 04 Dec 2021 00:25:46 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7c2fbe541728d81f3dfaf06e8f42a640efe0e87b82a659e7ed67a5893a505b38
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275795979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82981939a181510dbd1fe786b1827e2af507a856de32ebe04bd1fb0e119d2bc3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:02:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:02:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Thu, 02 Dec 2021 11:02:15 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 11:02:16 GMT
ENV LANG=C.UTF-8
# Fri, 03 Dec 2021 23:09:13 GMT
ENV JAVA_VERSION=18-ea+26
# Fri, 03 Dec 2021 23:09:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/26/GPL/openjdk-18-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='fdf145c2819ef28edee67b7a6605bee89aefc505a1abea1686bec03fcba87c70'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/26/GPL/openjdk-18-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='14e35be6e99a093bd4d5666bd4d557ebb94ab9e03eab9e9ae0eb69fc7b3e662b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 03 Dec 2021 23:09:28 GMT
CMD ["jshell"]
# Sat, 04 Dec 2021 00:01:35 GMT
ENV CLOJURE_VERSION=1.10.3.1040
# Sat, 04 Dec 2021 00:01:36 GMT
WORKDIR /tmp
# Sat, 04 Dec 2021 00:01:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "665e35e8d7dd0996edaba36220fd5048fee95f5155ec0426f628f18770239821 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 04 Dec 2021 00:01:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 04 Dec 2021 00:01:55 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 04 Dec 2021 00:01:55 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Dec 2021 00:01:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595058421fcb005f80f2faa2434369885cb20645caed265e7b4912808701d893`  
		Last Modified: Thu, 02 Dec 2021 11:23:15 GMT  
		Size: 1.4 MB (1361242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3ae6eaaf71ca5255b4e4a7a36ede1f474a651492df8a3cac4e446c8323d741`  
		Last Modified: Fri, 03 Dec 2021 23:22:08 GMT  
		Size: 187.7 MB (187667054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf4d2232681528d2a6e32dc2e9cae56096c79d81047686d63f1140004448260`  
		Last Modified: Sat, 04 Dec 2021 00:11:43 GMT  
		Size: 56.7 MB (56710120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b73f89b10df5a4a0e10e38c2d10caaef08c6c00d2b1db5ff6cd03637d203f4`  
		Last Modified: Sat, 04 Dec 2021 00:11:35 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4752fa793d04227137bcb90aeeafd163d21795c5008fbeb541a7973559aefc03`  
		Last Modified: Sat, 04 Dec 2021 00:11:35 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
