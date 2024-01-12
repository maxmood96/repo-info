## `openjdk:23-bullseye`

```console
$ docker pull openjdk@sha256:95ba1081ecebb718ceac00a8fb7bf005a31f7fe07b1d7ca297e12571988f135c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:5b08a11b8cb3f1d5446a1769fddea25bf200fe2f9e7ae9b35e9db94e68c0d028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342603385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d58274a17f09c23931ad3d4e9122076ba023457121e0d369545b257e6a7634`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 06 Jan 2024 01:52:17 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Sat, 06 Jan 2024 01:52:17 GMT
CMD ["bash"]
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 06 Jan 2024 01:52:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 06 Jan 2024 01:52:17 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_VERSION=23-ea+4
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='9a68dc2301a1ab9d674095ba14205b79ba23dd83002077ae6777edc820e789d3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a7293d34fcb6c1b9f5b0bfc74aabc4e695b0e6d6b6778172d59596b19db6e4e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
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
	-	`sha256:20006b2988c00b02609319a4b9c01b6ef97e870acf0223f60ff3a8ad46aa1709`  
		Last Modified: Fri, 12 Jan 2024 00:22:34 GMT  
		Size: 14.1 MB (14073050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b74a61ad870c3e8c1fa95ed4f992a6f5829cdd06431573dc7f00c57923391a`  
		Last Modified: Fri, 12 Jan 2024 00:22:39 GMT  
		Size: 203.1 MB (203106294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3b6073cc94b9e56164b7f96fe25f9f907867e27be80c51d27270de3806f590a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6974966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5812e8cbeb9ae6da02968f87cfd0afdcb168d9367cc5d9787c9452d56a7f7449`

```dockerfile
```

-	Layers:
	-	`sha256:34ca7b4436a878a503c69a2fbfccf627a228c9fa0eb65ff876fed9d4f5109564`  
		Last Modified: Fri, 12 Jan 2024 00:22:34 GMT  
		Size: 7.0 MB (6956076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a84cf150896f3f779ae13756235e05b29bdb61a4456c815d7b2d5c0781ef07c`  
		Last Modified: Fri, 12 Jan 2024 00:22:33 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:89f716dc21543ad7b9dc15473a58297fd93e88f1d038225aacd60cd13de4ba39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340693741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33bc3cc47f3fe00d195cf73e0091aebb1cb173d7c4caeb93221ff87609c4b549`
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
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 06 Jan 2024 01:52:17 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_VERSION=23-ea+4
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='9a68dc2301a1ab9d674095ba14205b79ba23dd83002077ae6777edc820e789d3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a7293d34fcb6c1b9f5b0bfc74aabc4e695b0e6d6b6778172d59596b19db6e4e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
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
	-	`sha256:f02a1eed168dc1eb5896335adfea6d24a1c1015853b8db73a0c6b6c9838d83c7`  
		Last Modified: Tue, 09 Jan 2024 02:21:15 GMT  
		Size: 201.0 MB (201007959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:505963e92d7ca1bd8bb2be0d142fe6befd87624d6c0ef53edf78968d209e83da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25592a4fe383c40dc4f5dfe71dd77224d87ae15f149346d0b5c5c9a736ad473a`

```dockerfile
```

-	Layers:
	-	`sha256:a0fb9455a767845c02e564b52ce1619a79d46dc75e0620cb3d874b1bdcd299d4`  
		Last Modified: Tue, 09 Jan 2024 02:21:10 GMT  
		Size: 7.0 MB (7043728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac143abe7563e02c264b10038b87c21a6f3d9b88bf573610ca2a16ef25ab32a`  
		Last Modified: Tue, 09 Jan 2024 02:21:09 GMT  
		Size: 18.4 KB (18407 bytes)  
		MIME: application/vnd.in-toto+json
