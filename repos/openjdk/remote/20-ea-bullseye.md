## `openjdk:20-ea-bullseye`

```console
$ docker pull openjdk@sha256:75215e0198360759c11705b4b11b46290cb63a60b573a26fa9b6871eff2960dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:8aa264d573a6f575e209cf3d4f224fc4a35fa53b6a92810e98015c6427ccc3dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336906298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9aab3ce809109f63e5143d5ee73b90eb4d9441f4d2f68b14611be0024e598f4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:54:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:55:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 00:55:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:00:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:00:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Wed, 05 Oct 2022 13:00:41 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 13:00:41 GMT
ENV LANG=C.UTF-8
# Fri, 14 Oct 2022 01:48:15 GMT
ENV JAVA_VERSION=20-ea+19
# Fri, 14 Oct 2022 01:48:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/19/GPL/openjdk-20-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='872bf878e925d040e586f05723275d769f00f5718745e0758e6345ab2ffa0b66'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/19/GPL/openjdk-20-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='3ea4c7aa0de5ed4d0e5e0d55d2ef9cfa261087e65af3fdf849ecb2186a414c0d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 14 Oct 2022 01:48:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47db815c6a4547dc224b75222193cb1851cf529d2cbdf26f854b9bbf97099b98`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 5.2 MB (5163279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf48494000001a037b72870d2a6a2536f9da8bc5d1ceddd72d79f4a51fe7a60e`  
		Last Modified: Wed, 05 Oct 2022 01:19:13 GMT  
		Size: 10.9 MB (10876505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a572f7a256d36a93ab0777949771b120c5d7dce75ea2a2d3d9444793b26b2ef1`  
		Last Modified: Wed, 05 Oct 2022 01:19:34 GMT  
		Size: 54.6 MB (54584293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec9184f949d7424381e024c08a4940ffa66da77a6cd8aaa1d9374b7f366f561`  
		Last Modified: Wed, 05 Oct 2022 13:05:37 GMT  
		Size: 14.1 MB (14071819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fef95053a4124bd26b153377d87b1c805f998c103d7e4a4a0dae86006770cb`  
		Last Modified: Fri, 14 Oct 2022 01:53:21 GMT  
		Size: 197.2 MB (197164154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e525621dd8a10cf87ba4484f2c801554510a95efc56f0fd364946bd9c9817129
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.2 MB (335232399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2204032f9667d2b65e7c5d7c0c9b5fc68d11fc9cd7632996bd8724dc001d450b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:23:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:23:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 00:23:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:26:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Wed, 05 Oct 2022 04:26:01 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:26:02 GMT
ENV LANG=C.UTF-8
# Fri, 14 Oct 2022 03:31:19 GMT
ENV JAVA_VERSION=20-ea+19
# Fri, 14 Oct 2022 03:31:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/19/GPL/openjdk-20-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='872bf878e925d040e586f05723275d769f00f5718745e0758e6345ab2ffa0b66'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/19/GPL/openjdk-20-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='3ea4c7aa0de5ed4d0e5e0d55d2ef9cfa261087e65af3fdf849ecb2186a414c0d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 14 Oct 2022 03:31:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37c953a37e989b49a533e8d08c80d87ce66fadee48160f9a4d8cd2dd5b0ec87`  
		Last Modified: Wed, 05 Oct 2022 00:37:21 GMT  
		Size: 4.9 MB (4944361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98802a15fc60bda24c79203236f930586f1dba6218aa2b4c121cf0dbf5627b38`  
		Last Modified: Wed, 05 Oct 2022 00:37:22 GMT  
		Size: 10.7 MB (10657400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aff223bb11e201213e82ed9838541b6a63fd9276370f73ed0dbdd6efd73e32a`  
		Last Modified: Wed, 05 Oct 2022 00:37:44 GMT  
		Size: 54.7 MB (54681658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cd1b7c124d493606efa74bb734facd3be5b8f2603628d9c24fda9b146dd616`  
		Last Modified: Wed, 05 Oct 2022 04:34:43 GMT  
		Size: 15.5 MB (15527320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d889a0a8a10a006db75ec4821342aa310a5fb72f599929bcd6553014471a70`  
		Last Modified: Fri, 14 Oct 2022 03:39:35 GMT  
		Size: 195.7 MB (195721035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
