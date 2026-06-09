## `openjdk:27-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:5715a2eac6968a6039e32721d0031da2baa508b610c0059bbbf73ec224b294be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:49e4378187871de48cc199713c272126eb610da9fa2632d976491089b29844f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.0 MB (380959859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9086756fec0ca72c52ca70ca9ed996754c4a6c1880954af5df0bf2fa57544ac`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 20:06:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 20:06:30 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 09 Jun 2026 20:06:30 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:06:30 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 20:06:30 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:06:30 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Jun 2026 20:06:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa326d2d2ca33191c4390da76882a293f7e7da3775051957bf0dec003bfa474`  
		Last Modified: Tue, 09 Jun 2026 20:06:55 GMT  
		Size: 16.9 MB (16946589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce46e0688b9eb4eff556d4d26af9887b2f2d09730761e2d2477ee5e75a1aa655`  
		Last Modified: Tue, 09 Jun 2026 20:07:01 GMT  
		Size: 227.1 MB (227070013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:8ffc4827ae08ad21e4a93b9d85eb9dc78d23bc7424e9b004a4bc98dcdab7348d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8684295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3223b17544d0a0f513afeb634cd92ee8f558998e5aa440f2ee104b383156d9b5`

```dockerfile
```

-	Layers:
	-	`sha256:71716e34155a59c9f1c2ba02c38c950f4165d91e97ed94f1fafcdb9f500f374d`  
		Last Modified: Tue, 09 Jun 2026 20:06:54 GMT  
		Size: 8.7 MB (8666356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfa01ae5d6a5eaa2c7c831a8db158aad81dbe3e312455d444240f07b36e51e91`  
		Last Modified: Tue, 09 Jun 2026 20:06:54 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:78a7838d03625f1e207d979bcb08ee0dd6c1894008507e14b068fac483b43efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.3 MB (379256789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b662be29f54d827fd8754fdcbf1d995942b5ead0bc1ab582a47c9bec51dda8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 20:05:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 20:05:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 09 Jun 2026 20:05:47 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:05:47 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 20:05:47 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:05:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Jun 2026 20:05:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbced6cd8b50a5a1a212abd6a3d86a4b3b8175443c76f6738398c890bcf5a8e`  
		Last Modified: Tue, 09 Jun 2026 20:06:13 GMT  
		Size: 17.7 MB (17730423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc6b85ca4f842f16f7fb70e74d5afa0c1cc447232e982aa12512b3c42c814eb`  
		Last Modified: Tue, 09 Jun 2026 20:06:18 GMT  
		Size: 225.0 MB (225045885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c1fc1018be6639f270b999c0e28a94f31874034c1204c9b6e174c9f92af656a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8821259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9423afd57222a9b6e02e82c85ac5073c4ec55fa33892decc70ee3dd83ffa018`

```dockerfile
```

-	Layers:
	-	`sha256:59d2a8c33e9ff57729211180c4a6a3227fa457746d63b46c63521ddca9d53278`  
		Last Modified: Tue, 09 Jun 2026 20:06:13 GMT  
		Size: 8.8 MB (8803201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b87f096c4fc7d1898dceb4b3f3314a2d5680f9da44cacccbd6ec46771ced23`  
		Last Modified: Tue, 09 Jun 2026 20:06:12 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
