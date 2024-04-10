## `openjdk:23-ea-17-bookworm`

```console
$ docker pull openjdk@sha256:c00b662fe946dd2f14e1e43f6b7b653b51887a1a86669158d21caa4776e796aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-17-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:50005eff88e706ef72feb6d765850c00346c7f32507f10fb6be91faf2fe36199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365650427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cebf6881b8535c9e1aca8dc57d3ffd4a3248740210ad4f61387761f31c2c76a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 04 Apr 2024 18:48:10 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["bash"]
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 04 Apr 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+17
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='e7d451c3caeb76083337f090da37588acb90bb60417bff99ef160a3a8b730bfd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ede1afd67be11e1e99e13b78f8b3159c14107cc919920d0e1e30636f67b92b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be75de2110d41e72c9dad0e17e4ca39e2bc3141eb4b00e7eab3ed02cb8eaa7a`  
		Last Modified: Wed, 10 Apr 2024 06:54:03 GMT  
		Size: 16.9 MB (16945827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7791ccc4a29aaa5bee9ed843fb85db20adf3badb235d500bab0d12b6d20651`  
		Last Modified: Wed, 10 Apr 2024 06:54:08 GMT  
		Size: 211.0 MB (210956882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-17-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:77a0b133478843dec363d9e74265fcb5a72f3ca9bcfb2edae7b8148a21287c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8240556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec776e1b6a85416976c2954fd8681b7a89963b1a2c988d0825fccbab4e42ef5`

```dockerfile
```

-	Layers:
	-	`sha256:e50d5e42f79034d441c3cb6478b102dca7a521657bdb7efcb7447620c09a1122`  
		Last Modified: Wed, 10 Apr 2024 06:54:03 GMT  
		Size: 8.2 MB (8221649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad5676efe0f4a2924a53a7fb516308ff983c28cc990a1f37971a612a1cbded73`  
		Last Modified: Wed, 10 Apr 2024 06:54:03 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:24baa83f1f1bd09d4bb0586e58b7f8f0ff69da8b7e28cf72bd3b6e23708b9026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.7 MB (363740989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f47c3594213cdb45afdae32a315057c2d5de164de8318feb9faaccd59986d5f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 04 Apr 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+17
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='e7d451c3caeb76083337f090da37588acb90bb60417bff99ef160a3a8b730bfd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ede1afd67be11e1e99e13b78f8b3159c14107cc919920d0e1e30636f67b92b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17436a1bcc9ca1dbdb0bc455f606f09462af1bdc6826599ce5bce2e7ab9f1a93`  
		Last Modified: Sat, 16 Mar 2024 15:53:20 GMT  
		Size: 17.7 MB (17728967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da966f8272c21c1580d7d628e25e690615131a947ff891c38f61639310259bb2`  
		Last Modified: Fri, 05 Apr 2024 17:57:58 GMT  
		Size: 208.8 MB (208847248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-17-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:28e204f8419aa341ad57ff0f4f4e9e5d21cde8db69603b1f70e9480899356cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8384262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a286c9e83724f30ff44cb764ad46923c379f6a88ac65104a9a22c346fd4e0fda`

```dockerfile
```

-	Layers:
	-	`sha256:be642d15b7f95adfb67d0902061a50ec6403b31b94d2df2f72744156c72b5676`  
		Last Modified: Fri, 05 Apr 2024 17:57:53 GMT  
		Size: 8.4 MB (8365838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f9ccbb7ad90c81f10e16600b57cb6ebde08591c68ac86cd22822c1b09c3ad43`  
		Last Modified: Fri, 05 Apr 2024 17:57:53 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
