## `clojure:openjdk-18-tools-deps-slim-buster`

```console
$ docker pull clojure@sha256:24f67daf6956b876e091564caa856317d0acd6724b4a2f970e83b44884dee0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-tools-deps-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:72523977b311fb587333fe4874f069aa78be409f7f935fcd29f55ceaf98df718
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280663290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ca9da1d6c46dab53df3832b3c6afbfcb10e7583b65c56c07919eb49e3c4199`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:19:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:21:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 09:21:10 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:21:11 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:21:11 GMT
ENV JAVA_VERSION=18-ea+31
# Wed, 26 Jan 2022 09:21:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/31/GPL/openjdk-18-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='d57d6a205ea5a0b891490b6d9e45315f719ba92123775c4e0e3e76464504f7fa'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/31/GPL/openjdk-18-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='668f2637087591644db894f1f03c5782bb491fd4452b0c736ab7f6e70f1eb036'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 26 Jan 2022 09:21:27 GMT
CMD ["jshell"]
# Thu, 27 Jan 2022 17:08:03 GMT
ENV CLOJURE_VERSION=1.10.3.1058
# Thu, 27 Jan 2022 17:08:03 GMT
WORKDIR /tmp
# Thu, 27 Jan 2022 17:08:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "980168025a3827bd7ed9d5ab1681ce29808ac8e6cbced3ab6683db8b365b54df *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 27 Jan 2022 17:08:22 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 27 Jan 2022 17:08:22 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 27 Jan 2022 17:08:22 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 27 Jan 2022 17:08:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa8d0f5eb646a53df0b867301afa43404e868c540fdf170240578844dfd0d6b`  
		Last Modified: Wed, 26 Jan 2022 09:43:10 GMT  
		Size: 3.3 MB (3269688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ace2dc38398daafd17b62b34a7bb2a78b97096331531522d95391c30a508a`  
		Last Modified: Wed, 26 Jan 2022 09:46:40 GMT  
		Size: 189.0 MB (189021416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd1b86a39d23871915da3ae1f306f84bfe517b2d83e69ea37bf0cdefda64144`  
		Last Modified: Thu, 27 Jan 2022 17:30:08 GMT  
		Size: 61.2 MB (61217423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61233321bcfa05f1a80174a7c802f1197c258c29f42dca51463a55dd734e25ae`  
		Last Modified: Thu, 27 Jan 2022 17:30:00 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef76c6ed2fa5d41f450238719dc105324cb699fe1594d78c139f77c61f60d80`  
		Last Modified: Thu, 27 Jan 2022 17:30:00 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-tools-deps-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bf83453e686330bc8f6be4a33e90dfa533907d980587e948cf8301586e51b5bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277662932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d9d9ba626e56f7cd17d04ed05d5be3ec764e552e47021c766c4fe1f69ff0ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 05:51:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:53:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 05:53:13 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 05:53:14 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 05:53:15 GMT
ENV JAVA_VERSION=18-ea+31
# Wed, 26 Jan 2022 05:53:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/31/GPL/openjdk-18-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='d57d6a205ea5a0b891490b6d9e45315f719ba92123775c4e0e3e76464504f7fa'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/31/GPL/openjdk-18-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='668f2637087591644db894f1f03c5782bb491fd4452b0c736ab7f6e70f1eb036'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 26 Jan 2022 05:53:35 GMT
CMD ["jshell"]
# Wed, 26 Jan 2022 21:25:47 GMT
ENV CLOJURE_VERSION=1.10.3.1058
# Wed, 26 Jan 2022 21:25:48 GMT
WORKDIR /tmp
# Wed, 26 Jan 2022 21:26:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "980168025a3827bd7ed9d5ab1681ce29808ac8e6cbced3ab6683db8b365b54df *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Jan 2022 21:26:06 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Jan 2022 21:26:07 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 26 Jan 2022 21:26:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Jan 2022 21:26:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a5c9716b24a17043a5d8ede1303daffeaaa07ff0393fa14caed54f01154833`  
		Last Modified: Wed, 26 Jan 2022 06:14:50 GMT  
		Size: 3.1 MB (3118858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb130a9002dae95ffa39a11a09540a74920396c04ddea39d630c28cb1aeefd4`  
		Last Modified: Wed, 26 Jan 2022 06:18:34 GMT  
		Size: 187.8 MB (187753218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45cc5e7e540bfda94b343f73ab72586f461ab0e9ae8af015882c33bd5898cbd`  
		Last Modified: Wed, 26 Jan 2022 21:48:26 GMT  
		Size: 60.9 MB (60866609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3186799dc0e5245c6710491b91df6f8eabd56ef3831e9f9747b54c8362bd017e`  
		Last Modified: Wed, 26 Jan 2022 21:48:18 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07284a62053e21c6b83a9e1a96a4754fe0478e98f7be1abf249dc680282f7d`  
		Last Modified: Wed, 26 Jan 2022 21:48:18 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
