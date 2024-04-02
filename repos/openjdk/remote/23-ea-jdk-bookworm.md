## `openjdk:23-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:c8cc1f170020f1106f849fdd30f122d58a6aa75fe7d5140687dedda8c8bd07f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:6b82306764b17c05ea317c848e368eade91f7f58cb4df57b3ba688c1b235d85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.6 MB (365638330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8daf957c31c71c7e78c17ce1e66bdc8dc8ce5a36dfd10174effdefdee2fba09`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 29 Mar 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+16
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='9a5d2039ec965c15d80dbc5106c9e2f1c4a80975e18d308b55f0a3d892f24358'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d654c940f0c5b9ed7549f29066599b2caedbaf2ec45f3745ac35e265c288e2d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f899db30843f8330d5a40d1acb26bb00e93a9f21bff253f31c20562fa264767`  
		Last Modified: Tue, 12 Mar 2024 06:02:43 GMT  
		Size: 64.1 MB (64140360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6804874cd0daa496b0df4315811efbfdac14faa2e3a3d0821c373b60972eead7`  
		Last Modified: Mon, 01 Apr 2024 23:50:12 GMT  
		Size: 16.9 MB (16945923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f8bb956d248ed6e328ec54cf3e1058bb4f4aae591fdd71526efcb73817818a`  
		Last Modified: Mon, 01 Apr 2024 23:50:16 GMT  
		Size: 211.0 MB (210953117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:7506344a0a9ca1b57b7fcf45f2e68f50a8c57934e629ec5a3b12e4c7137f20ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8248110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad99ffda2a9e0095fb7c2a1ce380d9b89a3f6d102e7ac5885a0624ac661adc6`

```dockerfile
```

-	Layers:
	-	`sha256:309cca09418e0ed3a1ddeb4c9d17d9adb1a9aabbc9e06b24cca64ff591b5d21a`  
		Last Modified: Mon, 01 Apr 2024 23:50:11 GMT  
		Size: 8.2 MB (8229203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a371ba11ac512835c9dc8ed6be11d2069335c1431ac2891e4248d0add25f7a`  
		Last Modified: Mon, 01 Apr 2024 23:50:11 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:26110c9ddf4fc5134729ff5272652d13c5ae32257825ac724f07387b05c8e525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.7 MB (363733140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89a976632b542126ff0f3a2265b774d0e68d4ef820723c4a78bd36718feeadb`
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
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 29 Mar 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 29 Mar 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 29 Mar 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+16
# Fri, 29 Mar 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='9a5d2039ec965c15d80dbc5106c9e2f1c4a80975e18d308b55f0a3d892f24358'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d654c940f0c5b9ed7549f29066599b2caedbaf2ec45f3745ac35e265c288e2d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 29 Mar 2024 00:48:11 GMT
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
	-	`sha256:a69502905d06834a39d5652cecda7a0382370ffb314262675689af6806c3de79`  
		Last Modified: Tue, 02 Apr 2024 02:49:25 GMT  
		Size: 208.8 MB (208839399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ff65313754c012078735b8a37a3a5b4f48f32a26e83db45bcccc382270b71304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8384262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538d5abf5122c699f7d138b31c3e791a6eaa524d68e970b5d01cd00345bc5136`

```dockerfile
```

-	Layers:
	-	`sha256:e035a1ffb5a3b849144b1272acd3cb4950dac531ab10af799e868b26ebba69a0`  
		Last Modified: Tue, 02 Apr 2024 02:49:20 GMT  
		Size: 8.4 MB (8365838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a44ac6b22d02a8f3cbf84917d63e1d2541f2d1f4f28e9d52bb431ccb42ca95f`  
		Last Modified: Tue, 02 Apr 2024 02:49:19 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
