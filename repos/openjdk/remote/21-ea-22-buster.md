## `openjdk:21-ea-22-buster`

```console
$ docker pull openjdk@sha256:c59401cc9a850a22c8b396e914fa6400d780519ea8252bd4eac3a036692f7216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:21-ea-22-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:3917db3be67f3c476a11f4b8f613656f71bd6bec544b1348fce09d5234201168
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336131675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06048fd5342acc0c93524b034ddeaa6c93f9173a86973d6873f863a0c30c61e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 May 2023 23:47:07 GMT
ADD file:d176a72312205fc75b2950df98f4ed25abadd4b053b9d85bea67466a5b30220f in / 
# Tue, 02 May 2023 23:47:08 GMT
CMD ["bash"]
# Wed, 03 May 2023 19:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:00:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 11:16:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 11:16:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-21
# Thu, 04 May 2023 11:16:35 GMT
ENV PATH=/usr/local/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 11:16:35 GMT
ENV LANG=C.UTF-8
# Thu, 11 May 2023 23:02:46 GMT
ENV JAVA_VERSION=21-ea+22
# Thu, 11 May 2023 23:03:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/22/GPL/openjdk-21-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='6ae3958a32809960b925b0fc4fae2236b5640c92b015274035fe3fb3ceb94f98'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/22/GPL/openjdk-21-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='c9afb1a0be1b35ed1e61bab79d5fec466f7e5c42b65bd8a65595d6699d0e77cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 11 May 2023 23:03:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a94073ab46f8d565f5938cc345d32f7adda10a2585e39555079da9d4ee595974`  
		Last Modified: Tue, 02 May 2023 23:50:40 GMT  
		Size: 50.4 MB (50448697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f81a21db4398b2051d4ceafd0420bc7966513f9baf20519c7d81761fa4905c`  
		Last Modified: Wed, 03 May 2023 20:14:08 GMT  
		Size: 17.6 MB (17580548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d5332f45f85796fad1c6f0f23d6efc4cf25b2cb5679e54d165c3c1f1f7839`  
		Last Modified: Wed, 03 May 2023 20:14:23 GMT  
		Size: 51.9 MB (51878971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b4fe5b2a90813f8e613e7bfa2865346dfa7b3f6ced4d25a336326d1c2d5fc`  
		Last Modified: Thu, 04 May 2023 11:17:50 GMT  
		Size: 13.9 MB (13927656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6237005ceeb3618c51a684f655f88562f793c88a64a5c7b4e640ba1dd3ba4f63`  
		Last Modified: Thu, 11 May 2023 23:06:38 GMT  
		Size: 202.3 MB (202295803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
