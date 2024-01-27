## `openjdk:23-jdk-bookworm`

```console
$ docker pull openjdk@sha256:5f44c65dd6cd385b764b9a9f70b95a90a3bc5f39dcc328c7c0c571ecbaf1a282
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:89e5398fd043a80a4353f81d36cd8d303d03f202fdec49e7f9286670e5f95b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 MB (357928194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cea36feb3ad5203d4d8b9f7e2a2da4c484c162966305ead1e402cfdc8fcb045`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:35:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:31:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jan 2024 01:56:28 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:56:28 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='b10ac9dc80cf8dd508c44072989f1327a05a95dfcbf0af1fc65571ac2de613a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='b21ca578927851a80700167439bbb9cd75c7d60152d51240bac49be8dd548e7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d85599795460b2d9d24c6b87c53ec60555b601705cc83bea31632240500980`  
		Last Modified: Wed, 17 Jan 2024 02:00:06 GMT  
		Size: 64.1 MB (64139892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a15b643a5e8140bb8d705f46127c03974ab2301478ee23e92ec6ceff99f29b`  
		Last Modified: Fri, 26 Jan 2024 23:50:12 GMT  
		Size: 16.9 MB (16945658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c93a0268386a7da50e1d8e4e34e5524627a844c246333adf658672a3aff42f`  
		Last Modified: Fri, 26 Jan 2024 23:50:15 GMT  
		Size: 203.2 MB (203234660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:770e41ae72cc12d578b52c6e929f3bc110559b9f9537bc895f6c1f58f448d1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7135242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db22e077e62cddb568c252facbf4db06badede28f63deb9174637ed76d12c01e`

```dockerfile
```

-	Layers:
	-	`sha256:7e4a1b5b328f4a67e140440c0f9b6b4029b86dc96e887dc203a4a33a419b425d`  
		Last Modified: Fri, 26 Jan 2024 23:50:12 GMT  
		Size: 7.1 MB (7116352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccaf91d811691342553a7d1901676adc2695c3f174908d52aa4a9c7dbccd859d`  
		Last Modified: Fri, 26 Jan 2024 23:50:12 GMT  
		Size: 18.9 KB (18890 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0db2015f6f3e14441e6cb1311a28182527257871892f374bd3ec837c84d7974e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (356032202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dca30ef61e8e95f01b9bad099c39fc1bcb1b633633766f8c2ce82935fa8def`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jan 2024 01:56:28 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:56:28 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='b10ac9dc80cf8dd508c44072989f1327a05a95dfcbf0af1fc65571ac2de613a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='b21ca578927851a80700167439bbb9cd75c7d60152d51240bac49be8dd548e7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b4f1810f998c1f1580e2404b2e7fed8e264902d898bbe531443ea9789b7641`  
		Last Modified: Wed, 17 Jan 2024 02:58:02 GMT  
		Size: 64.0 MB (63991147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb32b79503545458e2fc627360a71ead33be25914626cc424d8226cc3b833f89`  
		Last Modified: Sat, 27 Jan 2024 20:35:05 GMT  
		Size: 17.7 MB (17728784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d2ee8d73bd4d57a60283838d152f8e3455be84c460554b0cd46ee34478a62d`  
		Last Modified: Sat, 27 Jan 2024 20:35:08 GMT  
		Size: 201.1 MB (201137432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f11fce6ec5e18a2516461055ea8d4fb02546a5517b96b1f7f21d7e2650b5613c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7254087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398a73f651d571f16d6d1d048c63f55979c3bfb0428b0de9a0ec6f5a98fac88a`

```dockerfile
```

-	Layers:
	-	`sha256:b010a04862370f112138b6f319d58e926ceac3e4b13bea7fcf1e550b54266303`  
		Last Modified: Sat, 27 Jan 2024 20:35:04 GMT  
		Size: 7.2 MB (7235183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c89dfd1b7ac78b85412d8705d1b8f79a4cb4407e6288be92c065be92e1e5fb9d`  
		Last Modified: Sat, 27 Jan 2024 20:35:04 GMT  
		Size: 18.9 KB (18904 bytes)  
		MIME: application/vnd.in-toto+json
