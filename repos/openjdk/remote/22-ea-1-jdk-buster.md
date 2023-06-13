## `openjdk:22-ea-1-jdk-buster`

```console
$ docker pull openjdk@sha256:436243b06c7c690a476e8890f82f5f987025f7e6f91ec0c9f6a9764640a7d8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-1-jdk-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:b98231853919b740acf3c7c6815c3b7c5918a63f515c99813851ea7e733acf80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338671257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289ad5fd0f1767b02641f9135385db67fb406d3bfb317a830fb4cf85b808a9ab`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:48:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 12 Jun 2023 22:27:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Mon, 12 Jun 2023 22:27:31 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jun 2023 22:27:32 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 22:27:32 GMT
ENV JAVA_VERSION=22-ea+1
# Mon, 12 Jun 2023 22:27:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='50bf6303955ea128be3eb7ad9bc10f5e7eeacf9d3f81349a4d60a164fe7d0318'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ca14677cb2db094acbc9b084d0a85c9e004aff9826977e0b9b35e5f9a55b550'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Jun 2023 22:27:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4f22c742c8c8c929ee946913c0d0484c2e4ca28ea45a5ef8cebea022a33e00`  
		Last Modified: Tue, 23 May 2023 07:51:12 GMT  
		Size: 13.9 MB (13927723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e81dde938227f401b75bd9c5523b35bf6aa3676b25b32b0697833646d7a735a`  
		Last Modified: Mon, 12 Jun 2023 22:31:38 GMT  
		Size: 204.8 MB (204835632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-1-jdk-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0758e33b1d4b30abc2f9dd5d1f5f2e171d636677450a9dd9b87b1061d5d5e2d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336752867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349d966a54e962ebb3f2d32dbdbb7d1f027bdd45d6e1c8887496b994106392be`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:41 GMT
ADD file:bb3cb9e6abc423742d7c1b6bc006a7cef70038c5621c71a90a2ae7c1ea29ec63 in / 
# Mon, 12 Jun 2023 23:40:42 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 03:03:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:39:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Tue, 13 Jun 2023 04:39:23 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 04:39:23 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jun 2023 04:39:23 GMT
ENV JAVA_VERSION=22-ea+1
# Tue, 13 Jun 2023 04:39:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='50bf6303955ea128be3eb7ad9bc10f5e7eeacf9d3f81349a4d60a164fe7d0318'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ca14677cb2db094acbc9b084d0a85c9e004aff9826977e0b9b35e5f9a55b550'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 13 Jun 2023 04:39:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8371d57f7426517aead21bff5af0cf321625cac166c86214c439fb67db84243`  
		Last Modified: Mon, 12 Jun 2023 23:45:01 GMT  
		Size: 49.2 MB (49238409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7349847b3241e237d7a69174fea45593592e320324afdbae5c685b0a96e8181`  
		Last Modified: Tue, 13 Jun 2023 03:09:21 GMT  
		Size: 17.5 MB (17450037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f104dc4fba2c93f994673ea6c81b78ad44ef6b4d6984576abf9be7cf0dde960b`  
		Last Modified: Tue, 13 Jun 2023 03:09:35 GMT  
		Size: 52.2 MB (52217003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f38ddbccfa3900f9aeb3c809456e73e3ed25d3fa23aefc0a6a0a11d9fe5391`  
		Last Modified: Tue, 13 Jun 2023 04:42:52 GMT  
		Size: 14.7 MB (14672857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0388d0d44dfbdc9877a4fa2a06c77b4ad5a789524343a53050fa8b2ef68417`  
		Last Modified: Tue, 13 Jun 2023 04:43:02 GMT  
		Size: 203.2 MB (203174561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
