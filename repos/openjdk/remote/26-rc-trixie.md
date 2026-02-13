## `openjdk:26-rc-trixie`

```console
$ docker pull openjdk@sha256:56329a221ad878801c6f2aaa07f64a39840642a8754f0e6aa568eedbbe9c2362
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:60d870d2c982c29bf666d19377bd30fbab53d63aa930982a93a1039f8cd6066a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.7 MB (386746541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10a34d383ca86ea8bfeb684a11adcdd0d1386329ee4af8d6d9b83f1e05902b0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 12 Feb 2026 23:59:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 23:59:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Thu, 12 Feb 2026 23:59:57 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Feb 2026 23:59:57 GMT
ENV LANG=C.UTF-8
# Thu, 12 Feb 2026 23:59:57 GMT
ENV JAVA_VERSION=26
# Thu, 12 Feb 2026 23:59:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='e7c907ec1036e5480609f8212e6f1e7f710310e029d097e4e1a9645c43676945'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aeb9ccc00550a012197834334a9a6cbc03e7938774fcaf59dfa7ed158b66465f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 12 Feb 2026 23:59:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954d6059ca7bdbb9ceb566ca2239e01ef312165659d656753d7dbace7771a591`  
		Last Modified: Tue, 03 Feb 2026 02:43:06 GMT  
		Size: 25.6 MB (25614010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e2021c4c8bd1a46b34d9608a9381afdc333600ee1ef3c94306ecf7373e1956`  
		Last Modified: Tue, 03 Feb 2026 03:29:16 GMT  
		Size: 67.8 MB (67787365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd4dcb87b4f377436783d2a41793e87ff20476f17fe6ef64b593ca7d554a7a0`  
		Last Modified: Fri, 13 Feb 2026 00:00:22 GMT  
		Size: 16.1 MB (16062907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c87fc6ff2630c4d3fd2aaec13979a5639a237f5893647de7d2ce344bafe5c5`  
		Last Modified: Fri, 13 Feb 2026 00:00:26 GMT  
		Size: 228.0 MB (227989307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:ce5b1c53fef516cbe1e02de8d4d04dda5b75d74642b00f4e9d8d449009769394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550de8d2859347a79d92b224bb0ec620606f50c2c30b8be5cdadc2198db9378a`

```dockerfile
```

-	Layers:
	-	`sha256:bc20ddfae0c5d88bf12b1b0177d961550a5f34eac8d3b05fbe23f67bc2232dba`  
		Last Modified: Fri, 13 Feb 2026 00:00:22 GMT  
		Size: 8.5 MB (8510362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a98232cdf984c689c68ee5e6ca63426a2ce00da86cef4fdd1e897ae93452bd86`  
		Last Modified: Fri, 13 Feb 2026 00:00:21 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:71ba28562e976d93b64347dc8b3cc42193ce2f812eb62d38ea7f7bc8ace0eac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384242085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc18d808b020ed8b55499dcbc4a668f33234a065af963e8ed1a7afd9a9b09d1a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 13 Feb 2026 00:02:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Feb 2026 00:02:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 13 Feb 2026 00:02:50 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:02:50 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:02:50 GMT
ENV JAVA_VERSION=26
# Fri, 13 Feb 2026 00:02:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='e7c907ec1036e5480609f8212e6f1e7f710310e029d097e4e1a9645c43676945'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aeb9ccc00550a012197834334a9a6cbc03e7938774fcaf59dfa7ed158b66465f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:02:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cace8fbd9245d4cb1b11d410baa101c40f315e70bee7d3ba014bb966a4da4517`  
		Last Modified: Tue, 03 Feb 2026 02:46:11 GMT  
		Size: 25.0 MB (25022688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8128ce97ccffb1094b6eafc78b5827499d0496944f3d357e222bfc29f01968`  
		Last Modified: Tue, 03 Feb 2026 03:47:30 GMT  
		Size: 67.6 MB (67593005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad03b24ee9c291de9b41c89534b02ee654249ba7739495f87cba06f56e40c82`  
		Last Modified: Fri, 13 Feb 2026 00:03:15 GMT  
		Size: 16.1 MB (16071530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6105e9cb1907a0cb7bf4fa95f00151ca8be4ef3f53c573223435236158ce6a`  
		Last Modified: Fri, 13 Feb 2026 00:03:20 GMT  
		Size: 225.9 MB (225902845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:e4143b39d1feb7b58fc3476623e64f77a0a33522fde977817dae60cb859c8ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068b95432969b5303e81e1e65dee1b9331798ce1c91e16da3c92cb67c5a0010e`

```dockerfile
```

-	Layers:
	-	`sha256:d62984a071d2ae9287e002b7b2ffa1ec671b131fc603bdf6d3dad0927a5bd45a`  
		Last Modified: Fri, 13 Feb 2026 00:03:15 GMT  
		Size: 8.7 MB (8705128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eed7947863418c42092363f402d0f6a531c07e87a78434eb87e26ca6e48ca40`  
		Last Modified: Fri, 13 Feb 2026 00:03:15 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json
