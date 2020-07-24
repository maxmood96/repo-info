## `openjdk:16-ea-7-buster`

```console
$ docker pull openjdk@sha256:2751ac0ec0655df3c133ccd9cf539964ff92a9043462b58e38cf1a84bc70475e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-ea-7-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:31c1660c66510ff796ee87cd0660eae655e743aad318592d8c796c4b89cff724
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330544776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad5f0de586a472866228c40b4f52512ecd3918a751a672bac8e88984dfea658`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:16 GMT
ADD file:89dfd7d3ed77fd5e05f20a0ab631142207ae462f5bbd877f8745d3930c751d87 in / 
# Wed, 22 Jul 2020 02:03:16 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:00:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:00:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:34:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				binutils 		fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:34:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 22:34:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Wed, 22 Jul 2020 22:34:22 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 22:34:23 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 24 Jul 2020 19:14:11 GMT
ENV JAVA_VERSION=16-ea+7
# Fri, 24 Jul 2020 19:14:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-aarch64_bin.tar.gz; 			downloadSha256=0e2c7dc384e914fa785087a3970b0ab14f983447e55e663fe5a7b507104f9b7c; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-x64_bin.tar.gz; 			downloadSha256=e6d7f1485772b4ac0bdd4681af093a63eb1af7590efca05e950df04a25045a78; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Fri, 24 Jul 2020 19:14:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:31dd5ebca5efc5e96a425402fa85e492b02c8fe757dfd3edfdea2a7c67322909`  
		Last Modified: Wed, 22 Jul 2020 02:09:37 GMT  
		Size: 50.4 MB (50390325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed641c4ae9821ca3c399071ea82ae667237acbcaad1e367c3e1e87fc967834c`  
		Last Modified: Wed, 22 Jul 2020 03:16:28 GMT  
		Size: 7.8 MB (7811702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd57146431eae70720cf24877e818256ae1a30b9c1c9e7d0ad093c945ca0af2`  
		Last Modified: Wed, 22 Jul 2020 03:16:28 GMT  
		Size: 10.0 MB (9996319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac34a4d7c330794ec24a76e7e58b50d4c8f6a2fc77ca958d83092c8962e7d6d7`  
		Last Modified: Wed, 22 Jul 2020 03:16:44 GMT  
		Size: 51.8 MB (51829832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8eb5acf18e7b4ad9db90f79975b06b18325e8658a637c682f1cb13ed67997`  
		Last Modified: Wed, 22 Jul 2020 22:44:05 GMT  
		Size: 13.9 MB (13920343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616a5943f52c523b968db1fc8279d90b86f3aeb8c77c947c0b59763385cdd4c7`  
		Last Modified: Wed, 22 Jul 2020 22:44:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c265fa1cc2f5488d3771694594b8d331cbb632da326f97556b3f5aec56a9df`  
		Last Modified: Fri, 24 Jul 2020 19:19:14 GMT  
		Size: 196.6 MB (196596045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-7-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:90823ab87773836440bc7cbc859571a24051d16da1a14918c40b9e21f4cb6d15
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308827331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b669d99051c419992b67678c5700b09a51dbedef48f5f7e05f25e911262bdbcc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 22 Jul 2020 00:40:37 GMT
ADD file:14b8dca0bc0e6dae2f0bdb018a3a4e6d8d041abd03d118ae27cf7a72668f4970 in / 
# Wed, 22 Jul 2020 00:40:41 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:16:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:17:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:17:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 06:29:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				binutils 		fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 06:29:25 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jul 2020 06:29:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Wed, 22 Jul 2020 06:29:26 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 06:29:28 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 24 Jul 2020 19:33:49 GMT
ENV JAVA_VERSION=16-ea+7
# Fri, 24 Jul 2020 19:34:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-aarch64_bin.tar.gz; 			downloadSha256=0e2c7dc384e914fa785087a3970b0ab14f983447e55e663fe5a7b507104f9b7c; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-x64_bin.tar.gz; 			downloadSha256=e6d7f1485772b4ac0bdd4681af093a63eb1af7590efca05e950df04a25045a78; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Fri, 24 Jul 2020 19:34:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e2b2cb832ad58353bcc4edbdd16023beb64ec7856b469d202975f8de836c6906`  
		Last Modified: Wed, 22 Jul 2020 00:47:20 GMT  
		Size: 49.2 MB (49168473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d6493ea016bd1aa68fa88d01d53cd305f67bae5fa500592c76c466808bf221`  
		Last Modified: Wed, 22 Jul 2020 01:35:25 GMT  
		Size: 7.7 MB (7681419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33779eed82f6ae65801a87fd1278e902bbab0f609f0c6a0232d8ef0b37112127`  
		Last Modified: Wed, 22 Jul 2020 01:35:25 GMT  
		Size: 10.0 MB (9983891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59beb1d7f774f0b2aa38b8043218a6d924bda1eef4f4692efeae226cded00a94`  
		Last Modified: Wed, 22 Jul 2020 01:35:52 GMT  
		Size: 52.2 MB (52156162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742c26da5d081dda8dc535f97af15ccb22dee80c8f3f65c969b6ed36793624c3`  
		Last Modified: Wed, 22 Jul 2020 06:37:58 GMT  
		Size: 14.7 MB (14674125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beda4b2fcd73e863b96972f8bd7702708942641c008e45a0e284429d1e7aa0a1`  
		Last Modified: Wed, 22 Jul 2020 06:37:54 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4583b3f3397e747b7c35805e9865f48584ec2bde6aaaac20c99747bab26240a6`  
		Last Modified: Fri, 24 Jul 2020 19:39:25 GMT  
		Size: 175.2 MB (175163051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
