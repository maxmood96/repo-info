## `openjdk:24-ea-4-jdk-bullseye`

```console
$ docker pull openjdk@sha256:db6823ca9bd26cf8fedbb819eec6eaaa0dc22104109f122ee3845f1854844a4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-4-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:d259ba78404cf358a772007a0c327292d5e65718a2668d56636a4770024b3e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350926463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f8aca8eda9164ff88b0d03faaee8cb5e537846d95df92c0ac93574e8236414`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 29 Jun 2024 00:52:17 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Sat, 29 Jun 2024 00:52:17 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 29 Jun 2024 00:52:17 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_VERSION=24-ea+4
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='64aa493b28493a2d223626bdad774640cb148b0d52f392b081b2776532a980a0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d0b65f191528ab241b4e238568e52fa7199975b4f4b7badcf58a279b1fac426'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da238dd9d1f579bf4f3cd6589e3ab75747f8ea35be2bf50403f8f3fafa942eea`  
		Last Modified: Tue, 02 Jul 2024 02:01:35 GMT  
		Size: 54.6 MB (54588637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebe30c1ad22e3a8044199bd35d936cf182076e8b73446914b7822597777c3ff`  
		Last Modified: Tue, 02 Jul 2024 03:21:10 GMT  
		Size: 14.1 MB (14071295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5845ea81cc0e3af84db2a0668dc05db7b19d78d0ee0250871ac61064f414150c`  
		Last Modified: Tue, 02 Jul 2024 03:21:13 GMT  
		Size: 211.4 MB (211420997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-4-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:4327430f8161b7a3d47a1fdfa5beb3414fcd4482fb5b84164bb1dc27bfe968f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8175798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46be5fcc628f3d5048d97c66d67b31314ddb8b39738cee9c3a4928b0f70d3e4`

```dockerfile
```

-	Layers:
	-	`sha256:85755b43cd9356ad8b3fc0a11b5ea3f0b01e97c05f6ab46e7ded505ff2dbf547`  
		Last Modified: Tue, 02 Jul 2024 03:21:10 GMT  
		Size: 8.2 MB (8157352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc77950f35863ea05dc019069518427e2f1f904af8bbb7dacd619409b6a6c38b`  
		Last Modified: Tue, 02 Jul 2024 03:21:10 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json
