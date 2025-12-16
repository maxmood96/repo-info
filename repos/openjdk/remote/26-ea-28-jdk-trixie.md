## `openjdk:26-ea-28-jdk-trixie`

```console
$ docker pull openjdk@sha256:6575bf72c2b5716417438be9786c824da7cef4d1d812fbfe6e975dcfc7ddfb83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-28-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:581ed2386947210dae21ba8c4f21f0af80e8d8f761a13fc092e9ac62364188a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.7 MB (386689328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3f7f6dd76862dbf5f2d3429973d96e992f8d02c37f1a5002dda6ee19522739`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 16 Dec 2025 00:03:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:03:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 16 Dec 2025 00:03:22 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:03:22 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:03:22 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:03:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='a18910b0bdceb12a4f78147a1feebee50cc621ad8114c07a1ab071e58c17b09d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='d330a706e3fc611f4b39f6768f104e47d0a755ffabda31e3299dbc2e791f4f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:03:22 GMT
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
	-	`sha256:54fe1861b7ac17b3e9226407a7aed7261827884ff8022078d2e837ae40433682`  
		Last Modified: Tue, 16 Dec 2025 00:03:57 GMT  
		Size: 16.1 MB (16062724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7b4917887236bc70680cfb3b8324545fd673ccbb5843411190a435415de1a8`  
		Last Modified: Tue, 16 Dec 2025 00:04:07 GMT  
		Size: 227.9 MB (227944574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-28-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:e30176adecfa12ff2b9dfc3040664fc96467c2a52a1bd5fbbf9f68e7c2e95fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c96f302a7b5ce20e09b158b34906a1eb2b3b8c7d54fe872ea0aac16c2363a5`

```dockerfile
```

-	Layers:
	-	`sha256:7249461a380207614e72cb9bdd241175b26a781ae76a1a853244adb26238e200`  
		Last Modified: Tue, 16 Dec 2025 01:24:19 GMT  
		Size: 8.5 MB (8509979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3cc6f3da7aed8f52f0d3e6b5f8c34cb174a46c578eb63de13f2676b946490b`  
		Last Modified: Tue, 16 Dec 2025 01:24:20 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-28-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a6c824877982efc6577dc49cbb3fa39258a1486654639821d889eceb4ce31ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384183665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac47119896bca2ae4073bd1f1ebce9410071160d3b0825ed395e4004bc482848`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 16 Dec 2025 00:02:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Dec 2025 00:02:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 16 Dec 2025 00:02:49 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:02:49 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:02:49 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:02:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='a18910b0bdceb12a4f78147a1feebee50cc621ad8114c07a1ab071e58c17b09d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='d330a706e3fc611f4b39f6768f104e47d0a755ffabda31e3299dbc2e791f4f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:02:49 GMT
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
	-	`sha256:7c531c04f25588c1fd5b1d8fbd1b0bed38cd4f252217fa222bb885f7605a2ae5`  
		Last Modified: Tue, 16 Dec 2025 00:03:28 GMT  
		Size: 16.1 MB (16071498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce6972a52d5c09cbec405190f37eaf13048a20188969ad9b1ced7bffc85b0b7`  
		Last Modified: Tue, 16 Dec 2025 00:03:41 GMT  
		Size: 225.9 MB (225855986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-28-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:4dba0407ca01cb5e8a2e4a722b019bf12d8bf01d75c85b796abf521348f9d3a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dc0973a51dd07cf78114f634716b278bcbf5ab4c25b1b2f0a841a080814ac9`

```dockerfile
```

-	Layers:
	-	`sha256:088c1657582a4f629ffc4213c571bf7af1493ffa3997851526f2717be7e1f030`  
		Last Modified: Tue, 16 Dec 2025 01:24:27 GMT  
		Size: 8.7 MB (8704769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899d932f9b59e49114e648c38658a68cc453cbf54ca27ed4c6aa806a0bcfeb79`  
		Last Modified: Tue, 16 Dec 2025 01:24:28 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
