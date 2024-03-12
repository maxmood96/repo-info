## `openjdk:22-rc-jdk-bookworm`

```console
$ docker pull openjdk@sha256:db722f91a2ef7e4dc82e111229ee834a21f2c762cd229d954b6108685f696c69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-rc-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:19c7579151f0f4f547f5f0d9a698837922ab26a5b80e6c5278ad71a71c6ebaf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357565166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1eeabb310bc00aa4d95a7731a26e3175c2f8dc5e2bcdb3f866cbb89d60bddee`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Feb 2024 19:48:24 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 16 Feb 2024 19:48:24 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 19:48:24 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_VERSION=22
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f899db30843f8330d5a40d1acb26bb00e93a9f21bff253f31c20562fa264767`  
		Last Modified: Tue, 12 Mar 2024 06:02:43 GMT  
		Size: 64.1 MB (64140360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9664d01f45846c9648f5a998d038b2a34d658093980a718ed365dc6ce870e89d`  
		Last Modified: Tue, 12 Mar 2024 06:58:23 GMT  
		Size: 16.9 MB (16945837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b98ee6bfa68f75704aa283bd105a39ff77a51783062288805658224871acd03`  
		Last Modified: Tue, 12 Mar 2024 06:58:25 GMT  
		Size: 202.9 MB (202880039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0a7e3a5d3b57bd49453c9b4740a46d4db277dfa27317a43155bdf04276774cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8246858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e9752c087d14c03a1225521a3af2e8ac364e570ecfa67f3fc67e104ccdab10`

```dockerfile
```

-	Layers:
	-	`sha256:18b2cdd4905dd96025e7dde80be5274dcc0fc352f32f0d78138e18ec30588190`  
		Last Modified: Tue, 12 Mar 2024 06:58:23 GMT  
		Size: 8.2 MB (8228539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37d763f27145c31f81b4833cf7da202e57d84757b1ca4d232d027a5c1e0d1144`  
		Last Modified: Tue, 12 Mar 2024 06:58:22 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-rc-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dd1c059b7f8aa7d1745f2ca23d224fa2d6c90fd3edc26f30dbc0ddc5aa5f4310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.8 MB (355836057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d773a0aa917b4e34b5a80aea5c012d79c120bf9bd96f27247321d0a425d4bd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:37:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 16 Feb 2024 19:48:24 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 19:48:24 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_VERSION=22
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ae72c83b17aae41ce6857f0063bfd35b5f00dc5d7e1ad47fa18debb28b2c7`  
		Last Modified: Tue, 13 Feb 2024 01:46:49 GMT  
		Size: 64.0 MB (63990920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe14a5e4476942656d1cabdd2cbdcf3021e0b986bfb394a9bc0c3b1cac79b12b`  
		Last Modified: Wed, 14 Feb 2024 01:15:20 GMT  
		Size: 17.7 MB (17728893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45839e56acda2f369ac1e1a73e4a0f5abf8e6419f119be07d2424dbba08f8d49`  
		Last Modified: Sun, 18 Feb 2024 05:22:48 GMT  
		Size: 200.9 MB (200942513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:be4bc29ae7de0940c4483c22327f4c6ed6c7b574f8749badd4fdc8214e11b0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8383963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d79df10907addbbe9d28fcc53995f70a048256e0202f7f2d2c293ddfb5a61c`

```dockerfile
```

-	Layers:
	-	`sha256:485940d37d0658f5d0deac66c84b6339bbd625455810fcbdbb0265a1ee5b4327`  
		Last Modified: Sun, 18 Feb 2024 05:22:44 GMT  
		Size: 8.4 MB (8366131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9e2cb695a5d51e6f6d8c6b87a916b70eff05c67893c96f61985068385ea2e79`  
		Last Modified: Sun, 18 Feb 2024 05:22:44 GMT  
		Size: 17.8 KB (17832 bytes)  
		MIME: application/vnd.in-toto+json
