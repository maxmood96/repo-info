## `openjdk:21-ea-bullseye`

```console
$ docker pull openjdk@sha256:d8b4a3f146f2476f647fe0bdb0fe1183bba05bb38f999619f4bbacc6c75a7ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:ddc655f15ed09c1759db16c5adef987ec1cb32e667a9b0bbea4b83d9ea3415be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342476579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a61763f8ab0018f50e2041b88646e5eca81681c637488e40620374d8b201cd4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 May 2023 23:46:50 GMT
ADD file:fc290cf8ddb984325474583faa79c5a98c5ea0ec7f606bf360251f63acecf389 in / 
# Tue, 02 May 2023 23:46:51 GMT
CMD ["bash"]
# Wed, 03 May 2023 19:58:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 19:58:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 11:16:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 11:16:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Thu, 04 May 2023 11:16:09 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:16:10 GMT
ENV LANG=C.UTF-8
# Fri, 19 May 2023 17:24:15 GMT
ENV JAVA_VERSION=21-ea+23
# Fri, 19 May 2023 17:24:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/23/GPL/openjdk-21-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f3644497f76a889a341866ea29e2b3ce1c82772b1a0a827388d36cf2fd180263'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/23/GPL/openjdk-21-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='3241d3b6b20a9520ee937d7aab42daa55e86cc251ca77f0643e4425ccf7b1348'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 19 May 2023 17:24:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:918547b9432687b1e1d238e82dc1e0ea0b736aafbf3c402eea98c6db81a9cb65`  
		Last Modified: Tue, 02 May 2023 23:49:58 GMT  
		Size: 55.0 MB (55049070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d79063a01c561833dc6546d4e647fda0121a59e1a9a17874a3e30854555475e`  
		Last Modified: Wed, 03 May 2023 20:13:04 GMT  
		Size: 15.8 MB (15760340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eedd9c5abf7e5f63753a5e788cb0872a715fa1141e8ce5ea87638e6cd370a41`  
		Last Modified: Wed, 03 May 2023 20:13:22 GMT  
		Size: 54.6 MB (54584552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67c4f8ae7a4fcf76f00c258f20f64de21fcd40e356013a236207a5fc6fa71b6`  
		Last Modified: Thu, 04 May 2023 11:17:17 GMT  
		Size: 14.1 MB (14071916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb3a382e767166ebfd586cf36f4b46de2f64f657f7812523c5825e99b1dcea8`  
		Last Modified: Fri, 19 May 2023 17:27:18 GMT  
		Size: 203.0 MB (203010701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:53d16d38cee051020d35845dafe84f31a77f3336b21e3636447e1bde879f85a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (341000114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e608fcde5230d9893bed8478de44c8992700841a1140e159a1d47e67979fe3c4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:21:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 04:44:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 04:44:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Thu, 04 May 2023 04:44:02 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 04:44:02 GMT
ENV LANG=C.UTF-8
# Fri, 19 May 2023 17:48:49 GMT
ENV JAVA_VERSION=21-ea+23
# Fri, 19 May 2023 17:48:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/23/GPL/openjdk-21-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f3644497f76a889a341866ea29e2b3ce1c82772b1a0a827388d36cf2fd180263'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/23/GPL/openjdk-21-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='3241d3b6b20a9520ee937d7aab42daa55e86cc251ca77f0643e4425ccf7b1348'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 19 May 2023 17:49:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73587d290df17347645f166c8385f0a2d320a31f4803658f619f2887a5d88faf`  
		Last Modified: Wed, 03 May 2023 17:36:59 GMT  
		Size: 15.7 MB (15746737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd49b43770afa984b42a50282487e41b4ca05ba0e9f8bf233e6fc6d2fa99353e`  
		Last Modified: Wed, 03 May 2023 17:37:15 GMT  
		Size: 54.7 MB (54675990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb47cd2b57a6bbccf4f1ee3a3cafc8c5a39129694de56d517b087c5ae359ebc3`  
		Last Modified: Thu, 04 May 2023 04:45:12 GMT  
		Size: 15.5 MB (15528912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff09b9bca3c3fdae9bf43863dcd01cea1f1483c2698fce06048bb559293db354`  
		Last Modified: Fri, 19 May 2023 17:51:37 GMT  
		Size: 201.4 MB (201355770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
