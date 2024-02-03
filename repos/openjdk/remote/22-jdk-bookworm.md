## `openjdk:22-jdk-bookworm`

```console
$ docker pull openjdk@sha256:832759f74cb8032e44694e7044850cad37cc7329dbdbd16f7dbae60ecee93e1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d513a5129e78f09665b673ab5a9e26554ecef0566bee9da68a1728406680823a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357608506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e8a41939f7fcc3e7179f30dc53833a90a5f57e579a3473b90b273bd9cf041c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 19:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Feb 2024 19:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 02 Feb 2024 19:48:11 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:48:11 GMT
ENV JAVA_VERSION=22-ea+34
# Fri, 02 Feb 2024 19:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='170b7192de3e30c796b95d765b12ca457d3f4b05e97bee0bf81709c8b43cd992'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='63460b6a2c4d547d7a8cf4cf86d67a46f5e6a96a62843a787a2aabdbed4df119'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e92d11b04ec0fe48e60d59964704aca234084f87af5d1a068c49456b37fe3d`  
		Last Modified: Wed, 31 Jan 2024 23:32:37 GMT  
		Size: 64.1 MB (64142328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3221e8aef960686c01515d1c78c7c7edde6ee2f744f3bbd3d2b8d7c4db9add`  
		Last Modified: Fri, 02 Feb 2024 22:53:39 GMT  
		Size: 16.9 MB (16949196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0237ff24fb936ec9cdd8749314f918514a0a9ba773f1244bcec3ca1e40326b16`  
		Last Modified: Fri, 02 Feb 2024 22:53:42 GMT  
		Size: 202.9 MB (202883145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:81bfb209a8475c53f169e672780df2258c21a3aba75e63d58d0285a384f6c4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f965ef0c40b3e5be9c39d61950742335c36a10bee66979c96f9db13d0c61eb`

```dockerfile
```

-	Layers:
	-	`sha256:4aca47b017be4259f9e0e89d0d1d0863e44de289856745964c8d85770d02d2c7`  
		Last Modified: Fri, 02 Feb 2024 22:53:39 GMT  
		Size: 7.1 MB (7116367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42f13e8ef69139b9d4c117aec3c8496c3cd55450fae3e590abe9853533b644d`  
		Last Modified: Fri, 02 Feb 2024 22:53:39 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:94b33c18c0fa85cc07205e3fc9064d9593d6134bc5123b118126fccbac6edf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.9 MB (355866241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c382c0c1ad0183a6a8822740f61a82a3827370db923fa93efb30f1a8c274334c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Jan 2024 01:48:32 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Fri, 26 Jan 2024 01:48:32 GMT
CMD ["bash"]
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 26 Jan 2024 01:48:32 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:48:32 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_VERSION=22-ea+33
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='585ce01cf4908a98290ff33cc072d8733a012a58cb13a25304904bdb03c5e751'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='1df9746a0ac9f82fa421e32e0eaa4347dd657d612ca3e414c50b7e689ad59b43'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c812910e5e62436c8483e793d1956d1c70bcf42d20d5f0885ddafbe0ba124459`  
		Last Modified: Wed, 31 Jan 2024 23:52:23 GMT  
		Size: 64.0 MB (63994808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5985ce67cc9b5be13bbd1d05bdaef8d5b3eef2c56ba38018645982e475f95a`  
		Last Modified: Fri, 02 Feb 2024 14:12:30 GMT  
		Size: 17.7 MB (17732244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f42a8a2f43c0571fdf7d67b80dc9abf7877021d1abcbf30a090048f74bf1f47`  
		Last Modified: Fri, 02 Feb 2024 14:14:30 GMT  
		Size: 200.9 MB (200937445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ee9efdbbe6d41d4410e78565697ca14fc3c6dc7b1cf575b3cce8fc57a579501e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7253611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33dd3cf644f4a1f87d7780790ff6ab8a88cd5ce6464d9d2a2993282cff8d334`

```dockerfile
```

-	Layers:
	-	`sha256:d9bc845f7eee617d6d18a35f0cae52e68f73a8aeb18418fae35f4f0608e4cebc`  
		Last Modified: Fri, 02 Feb 2024 14:14:25 GMT  
		Size: 7.2 MB (7235187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dae2f8832a203d67e36f84ba8b1d49a552c637882ed7b55dfb91ee614a7d0fdb`  
		Last Modified: Fri, 02 Feb 2024 14:14:24 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
