## `openjdk:25-ea-bullseye`

```console
$ docker pull openjdk@sha256:4c975d9d160fd37d5f75e933d1c327f8b7ee48a28875005a81a16b3e048e7e90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:19bcbc14b685712b23ad180f0bd9d99c59c6ae6361f70fc09147e7ffeaab8eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351291836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6df827c166be2f9d2544937f3f0bff096c832e9f47d392c2a26ac04e5705412`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 10 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+22
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ce6d616a09c8fb4391dbe165428d33b1751a228581faf829ac0610db8120ddbf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='76b4d96328978d3ba01a6970ff47dd1f368e42e94a8ba51fb3260e07230de663'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Mon, 28 Apr 2025 22:15:30 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b357439c6bbf900764ff411893e648ec754a754e81a8c7d7c071411db7a0f2`  
		Last Modified: Mon, 12 May 2025 19:12:50 GMT  
		Size: 14.1 MB (14071465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8085d8bc08fb9523861ecf8b946174f4b25ca708b8fbacc7cd1c7692fd7c14df`  
		Last Modified: Mon, 12 May 2025 19:12:53 GMT  
		Size: 213.0 MB (212953081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:207799ac71427bc189eca29bb55049d746e9fb01e367707b8602db06b5df0959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8384808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd20d58181e08a09456f3acefaac05031f1e975087e970e4ccf907f4f9602b3`

```dockerfile
```

-	Layers:
	-	`sha256:f552aa32df0f1060fda120fb1c8706fe6ae83ddedcad2e71c953b23fc15a6c0a`  
		Last Modified: Mon, 12 May 2025 19:12:50 GMT  
		Size: 8.4 MB (8366190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1322ea463b7e1f0e109ade2698ecad023f1c68cae22bfd20fbacadc2cc6ff0a0`  
		Last Modified: Mon, 12 May 2025 19:12:49 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:473a059291ad6d2f13b0c3934fe68d184c1d8f0266df057803cf982a6e50b3d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.1 MB (349131944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd16ad8bcd167a5ecf66c31675cfec36499fd5cf5d733a850981207c75eabb9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 10 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+22
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ce6d616a09c8fb4391dbe165428d33b1751a228581faf829ac0610db8120ddbf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='76b4d96328978d3ba01a6970ff47dd1f368e42e94a8ba51fb3260e07230de663'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Tue, 29 Apr 2025 18:37:49 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e083c302b4f5ef95e7f103ab22b947c3e67397db7ff914707f08c59f2ec6b5`  
		Last Modified: Wed, 30 Apr 2025 03:54:13 GMT  
		Size: 15.5 MB (15526614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975117671bef6273576e7027cee681d5456ae21483414fb055c9332562480e61`  
		Last Modified: Mon, 12 May 2025 19:24:32 GMT  
		Size: 210.8 MB (210760242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:fe7e54c104b6fc1e85ed97eeebc76ddf90c7458c291ab683f76bbcf0df334b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8485913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ef304230e63da29642cb5e270c98d3dccc3c56e099f7c97c86dbd48a111221`

```dockerfile
```

-	Layers:
	-	`sha256:119c679c5d6665af4b07d6126b496689027257a0f6d3b373c64551280b19472b`  
		Last Modified: Mon, 12 May 2025 19:24:29 GMT  
		Size: 8.5 MB (8467152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacdc8073147df204017712105d7535b00c651a3c5c166d482304f2a4ed755cc`  
		Last Modified: Mon, 12 May 2025 19:24:27 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
