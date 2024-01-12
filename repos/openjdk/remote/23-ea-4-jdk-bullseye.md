## `openjdk:23-ea-4-jdk-bullseye`

```console
$ docker pull openjdk@sha256:fa067db81517b7cd9af194245dfc2c973ae2c7ddbc4316cc808b8b529bf43142
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-4-jdk-bullseye` - linux; amd64

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

### `openjdk:23-ea-4-jdk-bullseye` - unknown; unknown

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

### `openjdk:23-ea-4-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:50f07f7fa9e622262bbc1a839159ccb9fcab189d1eee87e692525d2a9c9c0082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340693743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049810ee7f13bd50cf43a90f24ad2e270df89477641398002c48ab6e4891e3ac`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 06 Jan 2024 01:52:17 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
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
	-	`sha256:3c6790303b4ce43016c9e2c25fc9c6f9d6c0de306f0665c77c6d0694ff6716e7`  
		Last Modified: Fri, 12 Jan 2024 09:22:47 GMT  
		Size: 201.0 MB (201007920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-4-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3e43c156cb34388374ef0b0b09283337cae2c94e02d933df7cccd7df877caba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c425ae7bf032ce14bc9672ef8c32c58b8ecc93cbf58e663157abb61abbc86f46`

```dockerfile
```

-	Layers:
	-	`sha256:b90501924f40c4392fde88e0be98904302f88bdc075918a73509d8b33b0c3dbd`  
		Last Modified: Fri, 12 Jan 2024 09:22:42 GMT  
		Size: 7.0 MB (7043728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c766d8a817e58052efa95af519e3b9524266331ffb28bd4ff563371fc39d436`  
		Last Modified: Fri, 12 Jan 2024 09:22:41 GMT  
		Size: 18.9 KB (18904 bytes)  
		MIME: application/vnd.in-toto+json
