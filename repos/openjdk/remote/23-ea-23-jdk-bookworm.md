## `openjdk:23-ea-23-jdk-bookworm`

```console
$ docker pull openjdk@sha256:5d1789be8bdd31677b307627ac1cad7139eb581f96fe8237f5371e0ab309955b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-23-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:72a3a5f440cdfdce010b6c6b6685decdf487aff448d6338dab646139d85d8725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364585097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e8929b433377cc486de3a9f11f2da965ab4ad673c0e8b4c93ebbb4b716ef15`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 May 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 May 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 17 May 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 May 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 17 May 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+23
# Fri, 17 May 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/23/GPL/openjdk-23-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='ebb29aa3b7c39ccf29ce564c797c5723b7355880f5dafd239570f7e7f2166bfe'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/23/GPL/openjdk-23-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='feef29529ab1660b95345ebbc6f47ba2823e28e87596225a25d2c45fc4537f29'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 17 May 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6582c62583ef22717db8d306b1d6a0c288089ff607d9c0d2d81c4f8973cbfee3`  
		Last Modified: Tue, 14 May 2024 03:04:25 GMT  
		Size: 64.1 MB (64142371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3c1666a075a9d7d14ac56ef089d57f33633927807966bc0f25f210fbe51d3d`  
		Last Modified: Fri, 17 May 2024 18:53:38 GMT  
		Size: 16.9 MB (16949314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5f2b916a2ef5c8bd71e237944e0a99654ed760eabd1e9246df76b19c85fa23`  
		Last Modified: Fri, 17 May 2024 18:53:41 GMT  
		Size: 209.9 MB (209866922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-23-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c1a1f26d29a791a11275935e2502a4e9443a5f112966912301344907a41bf9bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8240739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d867da4d417b1b315418cee9cfa038cfd5320876588d1259e8570835d5fcb2e`

```dockerfile
```

-	Layers:
	-	`sha256:b0b3e182f5a4d74bce624e2076e2dd2b3e1332fba970f4bd9f66d2bbc4fefc24`  
		Last Modified: Fri, 17 May 2024 18:53:38 GMT  
		Size: 8.2 MB (8221828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5a6c950aa7b9e8484f7fa8cfbc9a700d189494ddabedb3cd4843efb4d4fdb1b`  
		Last Modified: Fri, 17 May 2024 18:53:37 GMT  
		Size: 18.9 KB (18911 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-23-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ed073c83b7d1f6822183f75a617076d84dac791b5c41b7cb52c0f1acc619085c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.7 MB (362671163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8d32ae5a4d77f24f590d80c0866fd6a2b5140331ccceaab03c3893ed7e97d4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 May 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 May 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 17 May 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 May 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 17 May 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+23
# Fri, 17 May 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/23/GPL/openjdk-23-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='ebb29aa3b7c39ccf29ce564c797c5723b7355880f5dafd239570f7e7f2166bfe'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/23/GPL/openjdk-23-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='feef29529ab1660b95345ebbc6f47ba2823e28e87596225a25d2c45fc4537f29'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 17 May 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15856ca26414127b85cee6d10acbc4cee6eba9070f3f5a04b9cc72ce95abfa7f`  
		Last Modified: Tue, 14 May 2024 01:52:50 GMT  
		Size: 23.6 MB (23586610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ed4c12791345d3f20f66024e1f22275ce507868c508509b83dcf231b1c9adc`  
		Last Modified: Tue, 14 May 2024 01:53:09 GMT  
		Size: 64.0 MB (63994370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cfd4ecc181b3d5c8ef45bbbc5fa2651e9a869b37c87f87a6369c8a95e27013`  
		Last Modified: Wed, 15 May 2024 10:35:55 GMT  
		Size: 17.7 MB (17732480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7112b879cbfb42c400d37eb516be0123267356b69b505163fb3ad4f6f664123c`  
		Last Modified: Fri, 17 May 2024 19:46:52 GMT  
		Size: 207.7 MB (207744315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-23-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0480dd7a83893c1021b2ccbe9a03a03f6daed8f76fb1c7e7a85d068016d54b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5804a6574cb333c765622c3249203f72340e5eb45eebf320b8687bc902c123d`

```dockerfile
```

-	Layers:
	-	`sha256:88f31927de980e92f5ef31169217fd2c42221a86bc11b63b46a9fe949d4f9799`  
		Last Modified: Fri, 17 May 2024 19:46:48 GMT  
		Size: 8.4 MB (8359424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d305717da951100a4eb5a688e84573d6dc1db35ddd0ffc5949bc1be5edc52694`  
		Last Modified: Fri, 17 May 2024 19:46:47 GMT  
		Size: 18.4 KB (18428 bytes)  
		MIME: application/vnd.in-toto+json
