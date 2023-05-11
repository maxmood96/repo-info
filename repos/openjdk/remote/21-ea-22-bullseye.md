## `openjdk:21-ea-22-bullseye`

```console
$ docker pull openjdk@sha256:df9dfdecbfb9bcd2505deea1b905fdc4f82bcc943ed0e9259ade0749c9379b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:21-ea-22-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:533c645467b4a361d0784ef438efa0e52ce06b58aa1560b51e59d86a28532ae8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341751991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9191294b498d7ec023130cf915e58aba6d4925e2515dd7373a03b087ebe94d`
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
# Thu, 11 May 2023 23:02:16 GMT
ENV JAVA_VERSION=21-ea+22
# Thu, 11 May 2023 23:02:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/22/GPL/openjdk-21-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='6ae3958a32809960b925b0fc4fae2236b5640c92b015274035fe3fb3ceb94f98'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/22/GPL/openjdk-21-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='c9afb1a0be1b35ed1e61bab79d5fec466f7e5c42b65bd8a65595d6699d0e77cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 11 May 2023 23:02:26 GMT
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
	-	`sha256:a6e4b3998d817f633597f7931a36f531c0cef77197a5beb69812fd8a85a9283b`  
		Last Modified: Thu, 11 May 2023 23:05:26 GMT  
		Size: 202.3 MB (202286113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
