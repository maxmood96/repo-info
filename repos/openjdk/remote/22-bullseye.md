## `openjdk:22-bullseye`

```console
$ docker pull openjdk@sha256:005ddf999f7b97c927d9a48bc657be5ce13a65193fd2c4c79a43bc7c604c1025
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:85560bafa7bb66da129c688125980910f53b664d25338e2af5ba67b139f67b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342365215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11b0210717b88b4803797394e169d6e1b08bb2f7053029cf7b0821785d54e6f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:37:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c23b7d6528239a16f11d6e650e9a9fdb7039721df42b6ca01777fe34c2b116`  
		Last Modified: Thu, 11 Jan 2024 04:45:57 GMT  
		Size: 54.6 MB (54601205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a79e87d5d015fc9d98c380ba9e43531481715ace0a13990d3e10dc4aa473406`  
		Last Modified: Sat, 13 Jan 2024 01:07:37 GMT  
		Size: 14.1 MB (14072995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de0f5eb3a53b1553f333bd9d3855f123cd6946f3fffa6c5b3e9c6ca7fbad0dc`  
		Last Modified: Sat, 13 Jan 2024 01:07:41 GMT  
		Size: 202.9 MB (202868179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:2702adb613b64b1bd1ccb3b9f6afab1998f222039a65af615d5983a047be35ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6974991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09b39ebc76d5ce4c16cd0daede29a7f016c0046213a774a662991357b0a8a8e`

```dockerfile
```

-	Layers:
	-	`sha256:fdd342ff169b9aa97d71fa70f2f28cbd2c620a69a7ae79f2b63a40ad3d59f18f`  
		Last Modified: Sat, 13 Jan 2024 01:07:37 GMT  
		Size: 7.0 MB (6956084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72d3d1c009b21277efca97bf9e352766f58fce968f6a140ef26852a4a5980b39`  
		Last Modified: Sat, 13 Jan 2024 01:07:36 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dea66c8a959b3c9e189ae63de62c7cc4134828e7271081c4bdb24df6349295f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340613538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f1355de04320505797d58667db7c3a79b6d55560fadc05af752512e2479edd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 09:26:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 12 Jan 2024 01:48:33 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jan 2024 01:48:33 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 01:48:33 GMT
ENV JAVA_VERSION=22-ea+31
# Fri, 12 Jan 2024 01:48:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='389969d79769fb950fcaa9960610f90497af6fffb08bcbf1a88603450b58dc29'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/31/GPL/openjdk-22-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='662b370c327124f56151ec75cb7867c08a621c32eb8fdb2eabb0505af36331ce'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jan 2024 01:48:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebf2a961043d6b9dd703d0a485e216a2e302edf2e2525f7f410987d26905e71`  
		Last Modified: Thu, 11 Jan 2024 09:35:03 GMT  
		Size: 15.8 MB (15750711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826044e8ec1545c4af5dfe71ab63bce600198330f150aa968074bb86e78cd154`  
		Last Modified: Thu, 11 Jan 2024 09:35:17 GMT  
		Size: 54.7 MB (54699869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bfdfb22779e890668f0c60388a356f85eebf1e6ec064809ade715ec6947048`  
		Last Modified: Fri, 12 Jan 2024 09:22:42 GMT  
		Size: 15.5 MB (15527396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284d3ee8b6d0a1a1423502181043c3abd4649e8b2da20ecd59c18402bacbd55f`  
		Last Modified: Sat, 13 Jan 2024 01:46:56 GMT  
		Size: 200.9 MB (200927715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:006a2d1058be781e199ac30df13f561a99380152e3a0d685cf50a6798c56811d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fe5c3b21577aaae2ffe271062397488bcc61656390222fb316a6a0df951978`

```dockerfile
```

-	Layers:
	-	`sha256:52335b6269405c2e9aae67c2af16bf71d3752dbed31baaff0e31d3ef7a030928`  
		Last Modified: Sat, 13 Jan 2024 01:46:50 GMT  
		Size: 7.0 MB (7043732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccb035a1cc3f3687ef88ea8a2bc771a62c88e597d2e03ba16d03825f630cb701`  
		Last Modified: Sat, 13 Jan 2024 01:46:49 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
