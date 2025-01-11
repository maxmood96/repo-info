## `openjdk:25-ea-5-bookworm`

```console
$ docker pull openjdk@sha256:ad6d4a0db69687b0c0db68c82d81487898130d30d873059696555525e67116b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-5-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:f8aef961503d39b0ad7d8603e304dd0ee06a114e96e4f41f0e32c3cd43ef190b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366727407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea31c50b0f32d75dcbbde11c35e2ab1225ffbe445303b66de37fabd2193d541`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 10 Jan 2025 07:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_VERSION=25-ea+5
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b4ee63f91536c06f46e6f0d9c45e820bc2cb552046df27aa5c77d0bacc35aa21'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='43d1f9c863580d839b21121bc0c09ef0525d80ce1a3fbe26ea22fe2d77eadf7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
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
	-	`sha256:fcb1b10806c4b6163b37b9e762ea95219764679c578f752c295a89ddc97fac4d`  
		Last Modified: Sat, 11 Jan 2025 02:29:43 GMT  
		Size: 16.9 MB (16943039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888e8a1f300b344da20ee014257074c26921f145f0b6ce7d2adce6eec863457c`  
		Last Modified: Sat, 11 Jan 2025 02:29:46 GMT  
		Size: 213.0 MB (213030411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-5-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f27c2dfdcb2170b8274fc3198362fadfcca466c36f9697313679b809b816d71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8454827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d112a152fc4375b0dcf78e399e7702a95b70349d48ed8db672de7b29162432e7`

```dockerfile
```

-	Layers:
	-	`sha256:186a6149ab6d417d290f751f2a110577e0ea23a5d35dba9380bda7450771be7e`  
		Last Modified: Sat, 11 Jan 2025 02:29:43 GMT  
		Size: 8.4 MB (8436226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dae9580f059e6cec871a4b97e7c4b9bee324c3cd6b9efff364fe421970abd070`  
		Last Modified: Sat, 11 Jan 2025 02:29:43 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-5-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7b354c4c1dd7a8e7247a4d6068d6d1077e6e656514d0581b171cf123061bde41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.8 MB (364793006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9425c941fd25446fea03c2fa2987e8781155aa239a00ca7e63ca0bb74cb2abf`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 10 Jan 2025 07:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_VERSION=25-ea+5
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b4ee63f91536c06f46e6f0d9c45e820bc2cb552046df27aa5c77d0bacc35aa21'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='43d1f9c863580d839b21121bc0c09ef0525d80ce1a3fbe26ea22fe2d77eadf7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
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
	-	`sha256:3d195d4be860ba0fbb86b9aa0eb639820ae3cdd1548e956e6896df9f16cb2654`  
		Last Modified: Sat, 11 Jan 2025 03:17:03 GMT  
		Size: 17.7 MB (17726711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad4df102ee7e1d9e524144bbf934edc50e3de0f2584fc7e824d47ab2233653c`  
		Last Modified: Sat, 11 Jan 2025 03:17:07 GMT  
		Size: 211.0 MB (210987591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-5-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ad578933007183dd9a10fcdcf4ad29ea1b63cecfcf407c5a61a3c04fbbb16f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8591838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508d92200042afe4ace2006be7d58608aae466b66a10a25e537b984d92e37526`

```dockerfile
```

-	Layers:
	-	`sha256:1c97b4b9760d380312eac940c3b10a0cbc69fe066eb36e025126ce784525987c`  
		Last Modified: Sat, 11 Jan 2025 03:17:03 GMT  
		Size: 8.6 MB (8573094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a96d985bb08094308ba90568a14676ad442bda069ef8f144caaed65159e2064c`  
		Last Modified: Sat, 11 Jan 2025 03:17:02 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.in-toto+json
