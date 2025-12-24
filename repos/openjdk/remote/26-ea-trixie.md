## `openjdk:26-ea-trixie`

```console
$ docker pull openjdk@sha256:a78263f4fb9ddb7cd5a187594fce8d1d09d643bdb10949526022555e3119a8cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:9150d4243887927961cbe11a5ffac9e35f546af6401414fdcab209c7df056ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.7 MB (386702521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9588a797e822ccf749b263b73a70b717a93db07ef65b06bae9ed7d26e1b4ad7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Dec 2025 05:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:19:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Wed, 24 Dec 2025 05:19:42 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:19:42 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 05:19:42 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 05:19:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 05:19:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bdc0ec32229dcbbdc1521314b53e2a385f863589c5af85ef9f428798824654`  
		Last Modified: Wed, 24 Dec 2025 05:20:17 GMT  
		Size: 16.1 MB (16062728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1247beee28dc77a130d4508755c81cb287dedfcaf808d780bd063d1ea0207e78`  
		Last Modified: Wed, 24 Dec 2025 05:20:26 GMT  
		Size: 228.0 MB (227957763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:46e10781600cd27822519492cb290152962f344222fbc09cea6ff60e651b7208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2917298efd0a5ef5ec9fdecb159dc67695fb09425a4b60e77598593aee6c62b`

```dockerfile
```

-	Layers:
	-	`sha256:0fbb91ccd3ba78f9de7ecfe9abdfeeab564a66973cdd1c5b32670e91dff19352`  
		Last Modified: Wed, 24 Dec 2025 07:24:28 GMT  
		Size: 8.5 MB (8509979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95eb8803645fb179119ebde0454cce12eb031a0348b51c44bd31146b99a678b3`  
		Last Modified: Wed, 24 Dec 2025 07:24:28 GMT  
		Size: 17.9 KB (17912 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:af743bf5baac3f1f9420ca1c98df427e9d7b48a04b1992d03e8e79af1dc7045d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384197046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709844eb88bffaa69ede2c5f7df158926109e09f253fde400877ee834f8c3945`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Dec 2025 05:20:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:20:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Wed, 24 Dec 2025 05:20:38 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:20:38 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 05:20:38 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 05:20:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 05:20:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab65a9e27656d56384afac69b1f6d48552100db5c64996a517083211dd4b67b9`  
		Last Modified: Wed, 24 Dec 2025 05:21:16 GMT  
		Size: 16.1 MB (16071512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645a439eaedf176779a5e7dd63201ae30ad56e6ce219ae8b9c323619cf304613`  
		Last Modified: Wed, 24 Dec 2025 05:23:04 GMT  
		Size: 225.9 MB (225869353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:8b68d7ba97ead63e95f51c06f2686f18138ae9309bc8d23fef795868f3e491d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9628d007e20cdb53cb032b3e0044855700c7a36ff6bd848b97aa02d53b2372de`

```dockerfile
```

-	Layers:
	-	`sha256:50e9bf21f2bbc9cca920aae4bbda6e9eb191d92253740ad4ffad41a8dd04f9af`  
		Last Modified: Wed, 24 Dec 2025 07:24:35 GMT  
		Size: 8.7 MB (8704769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c67030b024e1a495e76444dd48a34992ce471c031eae3dc765fdbbc22d3f49c4`  
		Last Modified: Wed, 24 Dec 2025 07:24:36 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
