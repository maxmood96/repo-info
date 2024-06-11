## `openjdk:23-jdk-bookworm`

```console
$ docker pull openjdk@sha256:eb67a298d7db2ff35a5a8320f6dcc3bdbda11808f0b99d869ada305ca2c9d2c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:6653d00dfdfc25eeb37365a86d4c20a88a3b743bb9282a018a20315e562c390d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366111295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d42623e4d2d86f17c7552306827b01b27953c6507171f586bbd2e7015f257b`
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
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 08 Jun 2024 00:50:48 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Jun 2024 00:50:48 GMT
ENV LANG=C.UTF-8
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_VERSION=23-ea+26
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='a2a36c7b3c5fd89c6e392ba88a45a4647e482eab6b703595e2842e1b23c77ec9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='17a271b2853bc67590282ab01cceae8109012bc87ea2e07f7d5fefb55dd3192b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
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
	-	`sha256:1bfbcddca2cd0d1fd3fa61cb652cdae4b9dd1ef0409c3725bbaa542c53d9ff70`  
		Last Modified: Mon, 10 Jun 2024 22:33:08 GMT  
		Size: 16.9 MB (16949315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22916c6becee3c8d17926863ba04bab125e3a1def87e16ceebad2bd4af1eadb8`  
		Last Modified: Mon, 10 Jun 2024 22:33:11 GMT  
		Size: 211.4 MB (211393119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:318d1a1b498f06cb77e1886dc65803a0ffd1a7f3687ab38980b941df986c2dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8240290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fbdf407b008155abb7f2374f5619b1e948a49c1c04ea85a792f88d1661e847`

```dockerfile
```

-	Layers:
	-	`sha256:d53ad9adb27bf4fbf865e588863105423a5152b975dca93d3de1b33c59bb7636`  
		Last Modified: Mon, 10 Jun 2024 22:33:08 GMT  
		Size: 8.2 MB (8221827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08b209642354d1fc6a21b03b7e38c1fc9ef9fdf91ee059edb0c58daa67d0267f`  
		Last Modified: Mon, 10 Jun 2024 22:33:08 GMT  
		Size: 18.5 KB (18463 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ef4471eb936c21329cc8985068a1db6727233abcf446c03a2a9a0d9f76c1922d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364191520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c105206419a39a3afa79bf59ec9d572702ede0bcca343c6cef2ad9abc8bd0c`
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
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 08 Jun 2024 00:50:48 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Jun 2024 00:50:48 GMT
ENV LANG=C.UTF-8
# Sat, 08 Jun 2024 00:50:48 GMT
ENV JAVA_VERSION=23-ea+26
# Sat, 08 Jun 2024 00:50:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='a2a36c7b3c5fd89c6e392ba88a45a4647e482eab6b703595e2842e1b23c77ec9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/26/GPL/openjdk-23-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='17a271b2853bc67590282ab01cceae8109012bc87ea2e07f7d5fefb55dd3192b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Jun 2024 00:50:48 GMT
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
	-	`sha256:1afb03408eae01b37bbfde59ed4fa3cd5c5e7a323dc6f6848bd883163f052525`  
		Last Modified: Tue, 04 Jun 2024 11:26:44 GMT  
		Size: 17.7 MB (17732414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81974e304269ae6469a1d61f87e912b57615540faecb11f95c21bd128bda338`  
		Last Modified: Tue, 11 Jun 2024 03:38:27 GMT  
		Size: 209.3 MB (209264738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:796dfc49418503896ff8175e200b595ffb33602a51e54f0abf220da95b6a4a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8378291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48452ed712177ef22efabfe43791fa4d2fc23fe26181296c7258f607aa2ac846`

```dockerfile
```

-	Layers:
	-	`sha256:adb9ad3c9526513bf1583d302e35d8b56bac86749adc4ae3500587dbf14b463f`  
		Last Modified: Tue, 11 Jun 2024 03:38:23 GMT  
		Size: 8.4 MB (8359488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5412e18ff7f64910006e60a224aeb72332b5f8c3838ed0ca53af9728502149e7`  
		Last Modified: Tue, 11 Jun 2024 03:38:23 GMT  
		Size: 18.8 KB (18803 bytes)  
		MIME: application/vnd.in-toto+json
