## `clojure:openjdk-19-bullseye`

```console
$ docker pull clojure@sha256:d2c9d5a6acc5b9eb7bb3e0be4582a980c615e6849d1dce2ef84e659a91a734f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-19-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a7793cc20cee43d7d2bb4b337a587a947b3e92554466678a925c2bb41ebbbbd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355611041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c856280e85420d8bce5a259b80ba99d5c2074b96f8728028802dce5439f23a99`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 10:20:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Sat, 19 Mar 2022 10:20:15 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:20:15 GMT
ENV LANG=C.UTF-8
# Tue, 22 Mar 2022 01:24:09 GMT
ENV JAVA_VERSION=19-ea+14
# Tue, 22 Mar 2022 01:24:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='7c64317f728ce251b1fa6fcc612bbc5e4fac4d2862cf0f9b9edd98800072b6bc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='166aaa023baf2fff6484465efd16040557b4bbd57362409d730acec5d01fe749'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Mar 2022 01:24:19 GMT
CMD ["jshell"]
# Tue, 22 Mar 2022 02:26:25 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Tue, 22 Mar 2022 02:26:25 GMT
WORKDIR /tmp
# Tue, 22 Mar 2022 02:26:34 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Tue, 22 Mar 2022 02:26:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 22 Mar 2022 02:26:34 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 22 Mar 2022 02:26:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 22 Mar 2022 02:26:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292307d1c245e20dc8ed322b3b20edb2e71d1d52ef20d1671058c5141fb745b9`  
		Last Modified: Sat, 19 Mar 2022 10:36:14 GMT  
		Size: 14.1 MB (14071801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95de509c14fc258bc1bc007429c0d2788e28126a2166b6331777c253ff22be4a`  
		Last Modified: Tue, 22 Mar 2022 01:32:26 GMT  
		Size: 193.2 MB (193195765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8775c034565f64044537f4ac3255611d79e458378f69548a55253a973861ba81`  
		Last Modified: Tue, 22 Mar 2022 02:32:04 GMT  
		Size: 22.8 MB (22817135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc6406ee2807e5cd004050290166ac588f3632d715264e600147681b4366076`  
		Last Modified: Tue, 22 Mar 2022 02:32:03 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1becdd15be49705966e139b85d89274665a4cdc65609eb4bac00d2d396dcaec8`  
		Last Modified: Tue, 22 Mar 2022 02:32:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-19-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f5cf84da48579188dc16529312babb60528c0acb9b7e95c7c4e1d27df62b75cc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.2 MB (354213717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff56f85c85115c25b605419744c1b8e88ac47a2805539697d4d84af4595c5c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 22:11:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 23:19:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 23:19:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Thu, 17 Mar 2022 23:19:56 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 23:19:57 GMT
ENV LANG=C.UTF-8
# Tue, 22 Mar 2022 10:03:30 GMT
ENV JAVA_VERSION=19-ea+14
# Tue, 22 Mar 2022 10:03:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='7c64317f728ce251b1fa6fcc612bbc5e4fac4d2862cf0f9b9edd98800072b6bc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='166aaa023baf2fff6484465efd16040557b4bbd57362409d730acec5d01fe749'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Mar 2022 10:03:41 GMT
CMD ["jshell"]
# Tue, 22 Mar 2022 11:51:37 GMT
ENV CLOJURE_VERSION=1.10.3.1087
# Tue, 22 Mar 2022 11:51:37 GMT
WORKDIR /tmp
# Tue, 22 Mar 2022 11:51:45 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "fd3d465ac30095157ce754f1551b840008a6e3503ce5023d042d0490f7bafb98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Tue, 22 Mar 2022 11:51:46 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 22 Mar 2022 11:51:47 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 22 Mar 2022 11:51:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 22 Mar 2022 11:51:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399f445da611be3789923cf26d158e3f4f80449b7295fa069a8eaecaaf137e6`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 4.9 MB (4937558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9e43777fa6c09c341f3aa922f47b5b3ace26de1d779124afd2f1d435731d9`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 10.7 MB (10655858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81267e40a2df9e572fe797e45dbc086008422eb2216df18b7a91f1cf13e22b`  
		Last Modified: Thu, 17 Mar 2022 22:21:21 GMT  
		Size: 54.7 MB (54671322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3aa309b6e3524c3f3c38e901096dcffe1aad16e70f0d64aae615a9d7baac20`  
		Last Modified: Thu, 17 Mar 2022 23:46:25 GMT  
		Size: 15.5 MB (15524647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c3b3b7a83b694ed6dcc7c3bb1ca87cb17b94f1b3fd4e9d8ae4227a987e0ab3`  
		Last Modified: Tue, 22 Mar 2022 10:18:01 GMT  
		Size: 192.2 MB (192231221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4deb014b8bbca238794f646ab3c9e0330b2e3e440d10157adcfd3e6bb60d71a1`  
		Last Modified: Tue, 22 Mar 2022 12:01:13 GMT  
		Size: 22.6 MB (22575774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b975fa713b9087dc3ae9fa9ade3891b22d5443f4c147cb289ce7fdb3fe8b71`  
		Last Modified: Tue, 22 Mar 2022 12:01:11 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eceee9c625dfcc875e3019d0b2d8251286d6608775feca29d1b182be57f3f23`  
		Last Modified: Tue, 22 Mar 2022 12:01:11 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
