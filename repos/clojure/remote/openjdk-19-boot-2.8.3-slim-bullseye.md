## `clojure:openjdk-19-boot-2.8.3-slim-bullseye`

```console
$ docker pull clojure@sha256:ee25d760789feba4b914a970266bff79902faf195e80630992e63727df2d7504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-19-boot-2.8.3-slim-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:349ad442a7a35b22782539be18049e3ecc503b0c57e95ca9e41801450ffec563
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.6 MB (285645036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ae77cce26d699b12925c662becf0426fcc3c7314461cb7b89d7d097c4ae1bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 00:52:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 29 Mar 2022 00:52:15 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 00:52:15 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 00:52:16 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 00:52:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:52:29 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:52:02 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 29 Mar 2022 23:52:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 29 Mar 2022 23:52:03 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:52:07 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 29 Mar 2022 23:52:07 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 29 Mar 2022 23:52:07 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 29 Mar 2022 23:52:28 GMT
RUN boot
# Tue, 29 Mar 2022 23:52:29 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 29 Mar 2022 23:52:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 29 Mar 2022 23:52:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dc05f270bad654ee17f1143c48586c188a72929a128d61fd8ae15905d7b00`  
		Last Modified: Tue, 29 Mar 2022 01:04:32 GMT  
		Size: 1.6 MB (1582122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d100fc3e7b0dc5fbbf4534f7688cb06df0e07a6a9cdc51f10e7689f324fb53`  
		Last Modified: Tue, 29 Mar 2022 01:04:47 GMT  
		Size: 193.6 MB (193580462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1914dc4847b0a208e7bd830e1bc399ce3437520cd9cf3222048948924d02b24b`  
		Last Modified: Wed, 30 Mar 2022 00:12:24 GMT  
		Size: 283.0 KB (283028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08e264896529c929201ef3f3060888176c30227ad91fc8f2829a447508717c2`  
		Last Modified: Wed, 30 Mar 2022 00:12:27 GMT  
		Size: 58.8 MB (58820563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df94bec9d2b44aad1ee18daafec0a03c10de417f962f63aaec2f5ebde9481a25`  
		Last Modified: Wed, 30 Mar 2022 00:12:23 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-19-boot-2.8.3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78f9eaf6b6e1aab46da8701a5c77f6c45d9f8784a92de52b745dbd2cd9e3d78b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282590909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c67b772a74929ee355c2b4873c93abb7dddd5e380713905ff4cbba139262c10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 23:20:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 23:20:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Thu, 17 Mar 2022 23:20:25 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 23:20:26 GMT
ENV LANG=C.UTF-8
# Tue, 22 Mar 2022 10:03:48 GMT
ENV JAVA_VERSION=19-ea+14
# Tue, 22 Mar 2022 10:04:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='7c64317f728ce251b1fa6fcc612bbc5e4fac4d2862cf0f9b9edd98800072b6bc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='166aaa023baf2fff6484465efd16040557b4bbd57362409d730acec5d01fe749'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Mar 2022 10:04:03 GMT
CMD ["jshell"]
# Tue, 22 Mar 2022 11:49:45 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 22 Mar 2022 11:49:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 22 Mar 2022 11:49:47 GMT
WORKDIR /tmp
# Tue, 22 Mar 2022 11:49:52 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 22 Mar 2022 11:49:52 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 22 Mar 2022 11:49:53 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 22 Mar 2022 11:50:28 GMT
RUN boot
# Tue, 22 Mar 2022 11:50:29 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 22 Mar 2022 11:50:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 22 Mar 2022 11:50:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494f7f18e3d8fbed7417515196913f39c7c8b9fb93a63ebaa040b02f90ecde75`  
		Last Modified: Thu, 17 Mar 2022 23:47:05 GMT  
		Size: 1.4 MB (1361288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba04e38b91c9e0766a938bb44f843272845eee156dad1883f818fbc428967dc4`  
		Last Modified: Tue, 22 Mar 2022 10:18:49 GMT  
		Size: 192.3 MB (192282584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3ef3029872f0007d86f2fd097dd5ec91634779771a63324eb8252cb5f36687`  
		Last Modified: Tue, 22 Mar 2022 11:59:51 GMT  
		Size: 67.2 KB (67215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cba4f38b52a27cc017763f0063371328776f37d0ce9c1c1d9b82b2869a9f154`  
		Last Modified: Tue, 22 Mar 2022 11:59:55 GMT  
		Size: 58.8 MB (58816403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46acab3a9dc6dcc6d6785305c12ea8430c9c6f16595cdcc51b859d7905659d01`  
		Last Modified: Tue, 22 Mar 2022 11:59:50 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
