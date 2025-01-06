## `openjdk:25-ea-bookworm`

```console
$ docker pull openjdk@sha256:4470953d2a3f89c64470f4022b7d5d5c2a97c282a824d75ce25190c9a6e14ebb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:573ddb52ab71dade409d26843a0694bd9bc3e2b17a2ebcc1b13e37ff6e064176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366680284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3dcfe265530fb76b8bbb7b93443f8fd4d83630de0755766345069ac6ccb48e4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 13 Dec 2024 19:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_VERSION=25-ea+2
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='00d23f37267bee9e859091c506e986262ad9b7fc9f7818d3e9d602191252626a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='c3b55a9e0597d7942cadec32e1e920bdc4022d893bb4501ef8b54eb6a9ff2bd7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8176e6d893aff4b57b2c22574ec2afadff4673b8e0954e275244bfd3d7bc1`  
		Last Modified: Tue, 24 Dec 2024 23:16:06 GMT  
		Size: 64.4 MB (64391074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85d68a220e9495266eff87c134c9bde9bc0cb2c683162e497b84aaa4b51122e`  
		Size: 16.9 MB (16942963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756ab5fdef54fd11efdba661ac1fd903f30f0d51c05a3e6f4a94dc9c8ca1afb5`  
		Last Modified: Wed, 25 Dec 2024 00:14:03 GMT  
		Size: 213.0 MB (212983364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b491da46e13a67884b3c208188d3a0403509802e40fa310dd98e5270d589934f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8454827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b2f9ffbb348fa3004f8d524d2d45ee2454f7fbe6c3206212eaf4922d8daed8`

```dockerfile
```

-	Layers:
	-	`sha256:7848e357e2e79f2f628e2698176c040ac9f321a4ff1fa536bab5e5bad0306697`  
		Last Modified: Wed, 25 Dec 2024 00:13:58 GMT  
		Size: 8.4 MB (8436226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c843f4d1a3ec8a84709db1e99e3314e5216d020c07c08644dc083620584beccf`  
		Last Modified: Wed, 25 Dec 2024 00:13:58 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0bfa3803786d4598ca501727f4fcd60aa3d0524086dd3b9d2ce95e96db5f7b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364736509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d158588bab6844191bfd119443c29c5f4fff48d98d383551bf49616563d84d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 13 Dec 2024 19:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_VERSION=25-ea+2
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='00d23f37267bee9e859091c506e986262ad9b7fc9f7818d3e9d602191252626a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='c3b55a9e0597d7942cadec32e1e920bdc4022d893bb4501ef8b54eb6a9ff2bd7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745514a21aa2d3ad3fcaeb1ada9d14a783a87cb88541b06c3b2e2ee00c6df1de`  
		Last Modified: Wed, 25 Dec 2024 11:58:35 GMT  
		Size: 17.7 MB (17726648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3dd76ed5e371563b2078f6f735f27a1db89070fdf466877d6d9c8b71bd9ff4`  
		Last Modified: Wed, 25 Dec 2024 11:58:39 GMT  
		Size: 210.9 MB (210931157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:905e4d291390af183229ab633ce86c76d69e853a89fc59dc1964717519d3f454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8591838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420cbca210c30ca74101b8c3b0ad46d061b55e124a6e770dfdd5d97f57f42979`

```dockerfile
```

-	Layers:
	-	`sha256:fcfdba11fafc258db373cb627afa3e833f3e081126bcb740ccb64c617ce99cc2`  
		Last Modified: Wed, 25 Dec 2024 11:58:34 GMT  
		Size: 8.6 MB (8573094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02d22e983e552e627abd7566bcd710da2cfef1b1790870f6a66864cb0b2629b2`  
		Last Modified: Wed, 25 Dec 2024 11:58:34 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.in-toto+json
