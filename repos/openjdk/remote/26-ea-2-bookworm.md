## `openjdk:26-ea-2-bookworm`

```console
$ docker pull openjdk@sha256:76eac0411ef7bec92006a0f04c2a079b3aa6f989a15ff742af4d697a6706e559
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-2-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:aa0930943086e1ca7fb4ce93c30d265f8c4f4948fe459aecb8aee693caab1f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.0 MB (377040054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b902b32cdba821f061938095faa269adc2939eab3d60e56b7baff7de976677e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 14 Jun 2025 00:54:06 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:54:06 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_VERSION=26-ea+2
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='433a629dd1072b3147cce33cf79ae06ba8c7aa9aac53f403330e8f10ec12ca76'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f413ff4f8e92fcdeaf0da5315a51d2165a4017852a4a6c7e2731a8aae19e2e7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8257df6e15e2f7828b3c028be3fd8b87ea52f7b9f0ba37fc40bbbb35a215c9`  
		Last Modified: Mon, 16 Jun 2025 17:51:24 GMT  
		Size: 17.2 MB (17227508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdefbfd8bfba1142afef9871ee42abf4f21e82717dc07230578acb15f199cbdf`  
		Last Modified: Mon, 16 Jun 2025 19:02:59 GMT  
		Size: 222.9 MB (222902772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-2-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:21fe28ef530ec2293701f1c1b5a6faee6dafe37dcc8c1dde5d6cb43da43abcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8683787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc08e27b093f20aa6d9b4c5e0eb37ae089d2d53b25ef8d56640ab8a4d0f6c25`

```dockerfile
```

-	Layers:
	-	`sha256:e17f8578380c32ab2042b3a8b6ba0c91fef0921bebdca7a733fc08417da1680a`  
		Last Modified: Mon, 16 Jun 2025 18:25:24 GMT  
		Size: 8.7 MB (8665186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93c822e30469d4ca6620c6b8919e6208ac46f89e584010ea981c3f014b0946da`  
		Last Modified: Mon, 16 Jun 2025 18:25:25 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-2-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6ab758d2995899484d8c2cbea8eb32a729d1992e80b19e4bfb1cfeb80e99c57f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.9 MB (374947258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847799a36d3ae0419dc09efacb96fd325dbc25e12f28779326b6bf4c955c33e6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 14 Jun 2025 00:54:06 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:54:06 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_VERSION=26-ea+2
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='433a629dd1072b3147cce33cf79ae06ba8c7aa9aac53f403330e8f10ec12ca76'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f413ff4f8e92fcdeaf0da5315a51d2165a4017852a4a6c7e2731a8aae19e2e7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154371975b8325994bca32bb0a00994674b6beaa8c22ce78562c07918b7376b6`  
		Last Modified: Mon, 16 Jun 2025 17:52:18 GMT  
		Size: 18.0 MB (18014447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96de7b4b42be58b7da111a831afe7c3f643ebd61f1e73334ca3e6b59265b8c89`  
		Last Modified: Mon, 16 Jun 2025 19:12:46 GMT  
		Size: 220.7 MB (220679550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-2-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:6e467b0e4ab1db8c6f8295bd1aeaaa3fb821d1c95265ba01a5456d142c11087b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8820799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96ddd9e4e06ba079f99e7ee572ff31fb942a6198882ecff47fb099ed95c21c2`

```dockerfile
```

-	Layers:
	-	`sha256:6375af673831fd3980a5dd777d90298e7e2f9879db43e94efdfe00256ba5a669`  
		Last Modified: Mon, 16 Jun 2025 18:25:35 GMT  
		Size: 8.8 MB (8802055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50286b7f712de9e8e7441fe0d375cc55c1911d88ea8a55168ee3b14a85e9f797`  
		Last Modified: Mon, 16 Jun 2025 18:25:36 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.in-toto+json
