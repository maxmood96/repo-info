## `openjdk:23-ea-bullseye`

```console
$ docker pull openjdk@sha256:672d531b436aa707c2cf98e6679fcec40f01516b924ae9fd69a307aa9c95705d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:f13239b21b8e7a1a26cbf14651bb4271f54b7741d2192f2fa8c8beb8a76aec6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342590770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b36348f42159a6c9e3091a97e2f8e64ea141724f6267e17cade8bd0aac5df35`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:38 GMT
ADD file:d3a2f1f42338ba7066e352cea3b7bf4c7576e6b96fef785e8da763114f337c0e in / 
# Tue, 19 Dec 2023 01:20:38 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:33:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 22 Dec 2023 01:54:02 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:54:02 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_VERSION=23-ea+3
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='9dfa6ea30eef2154e14ec5e38358cc814e1c5a766b1e4f9b4eda8277086defe2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='52fc0b69ed616eaabc2c5d89fae1654ad188324ca52ece1dfd5f44edf6645410'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:18f2c3b7ca52caba205d748b9ce41784eb010ca83ece9e84e2a09130a5ec3cbc`  
		Last Modified: Tue, 19 Dec 2023 01:25:17 GMT  
		Size: 55.1 MB (55057340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8988ac7a69cc18b80883227d1cddd6babff98a5fce88b591500f8727dd26ff0d`  
		Last Modified: Tue, 19 Dec 2023 04:42:17 GMT  
		Size: 15.8 MB (15764812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d278fc41a93b35689afe55f7bbeda81194c3ed9d7162d8adf2ed2af1e042ea`  
		Last Modified: Tue, 19 Dec 2023 04:42:32 GMT  
		Size: 54.6 MB (54595440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1485e827f4e17bf8f13b0e6526b06f088c1ad7643d41d26a4647358c630f99`  
		Last Modified: Wed, 27 Dec 2023 21:53:50 GMT  
		Size: 14.1 MB (14073148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b02a890f6cd0bec564943d426951df698e71b805d26533c49445e37b42c887a`  
		Last Modified: Wed, 27 Dec 2023 21:53:54 GMT  
		Size: 203.1 MB (203100030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:a66413c01df2adc811d086b4193de5311c2af256cb1dd50c7275dc0331c5666a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6974966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b70616ab3336dc9900f22201df1cf3cc73d0868541cfacb21fb36798c87ecc0`

```dockerfile
```

-	Layers:
	-	`sha256:a2a890a9e4c3f75d0d13a3a31c26ba4f8baa6c8e56da6e77dc4f53c26eec2241`  
		Last Modified: Wed, 27 Dec 2023 21:53:50 GMT  
		Size: 7.0 MB (6956076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d852375db41a53f7dbb82ce83da6717c6a0c8774d4cfe42d9055a484c514c0c7`  
		Last Modified: Wed, 27 Dec 2023 21:53:49 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:143301948b7d383cb134a8bd4c8a7d81567127d9a9f0754ba3c3382a0d85c7d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340691579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8491dc7eef0941e23452c0a9523886f1b486fb95681e83114364fab1680a96e2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:17 GMT
ADD file:06ba7e39a2f8e1a7bcbb929fa9d1e6fb1f8bdcf5096dc903576af8f7014e353b in / 
# Tue, 19 Dec 2023 01:41:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:35:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 22 Dec 2023 01:54:02 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Dec 2023 01:54:02 GMT
ENV LANG=C.UTF-8
# Fri, 22 Dec 2023 01:54:02 GMT
ENV JAVA_VERSION=23-ea+3
# Fri, 22 Dec 2023 01:54:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='9dfa6ea30eef2154e14ec5e38358cc814e1c5a766b1e4f9b4eda8277086defe2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/3/GPL/openjdk-23-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='52fc0b69ed616eaabc2c5d89fae1654ad188324ca52ece1dfd5f44edf6645410'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Dec 2023 01:54:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:396a672fee8bade1a7c9f228d919717447f110f39046d8b5ed21ad45ae13ab61`  
		Last Modified: Tue, 19 Dec 2023 01:44:57 GMT  
		Size: 53.7 MB (53708091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010797996cc86cf2cf7495aebc22e5be7d18a10bde1e11562dbe5283c226c0e9`  
		Last Modified: Tue, 19 Dec 2023 11:43:17 GMT  
		Size: 15.8 MB (15750308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70092c2a6b382a0cc0bd2adeb187b94d74c8bcf2ceb6f33bb8e4e4e9c6561141`  
		Last Modified: Tue, 19 Dec 2023 11:43:31 GMT  
		Size: 54.7 MB (54699871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1785a2fc73cfe822cc337a8e52fcdac12a62b315d671510d5ed3cbc4a9e6d32`  
		Last Modified: Wed, 20 Dec 2023 10:23:15 GMT  
		Size: 15.5 MB (15527512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e76cfdcac24963bc498e7984504312ad2bb5650dc2f488fdbae95bdf2eb2df`  
		Last Modified: Thu, 28 Dec 2023 05:03:04 GMT  
		Size: 201.0 MB (201005797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:44e40fee916f4af105473169ae3d8faebe7be9d09a439911510b1cb793631896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa62ac843a59ddfbd2b45f486ea260ddc7858c3a04bcf848c7ca6309cd2aa3e`

```dockerfile
```

-	Layers:
	-	`sha256:18d30454763369e584ba20292d756a29680108d94d49e19cbeb322927822f54b`  
		Last Modified: Thu, 28 Dec 2023 05:03:00 GMT  
		Size: 7.0 MB (7043728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54d5e282fb46c61e80f1cf97800e8b353ccd49cdf387616a2e9f1fecec95f562`  
		Last Modified: Thu, 28 Dec 2023 05:02:59 GMT  
		Size: 18.4 KB (18407 bytes)  
		MIME: application/vnd.in-toto+json
