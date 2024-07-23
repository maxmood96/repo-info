## `openjdk:24-ea-7-bullseye`

```console
$ docker pull openjdk@sha256:7aaaf6b87681c3ee038dfffe25e746a8d2215a37a3613b41cadf4fc31d07956f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-7-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:14d374779055a8ad28c50a4d400090fd3b6d30ac9b326788cbed7072b3d4effb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351143497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8297cc4e9a548ae8954e428292cb168c18bf577ff47554d8897339b881115c40`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:50:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jul 2024 00:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 20 Jul 2024 00:52:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 20 Jul 2024 00:52:05 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 00:52:05 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jul 2024 00:52:05 GMT
ENV JAVA_VERSION=24-ea+7
# Sat, 20 Jul 2024 00:52:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='d175c4cfc7ab8306b42cf88fe0e60b2b827a2106c026ae6d2a3f2e51bbcb60d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='5df46f7b64a38a7a34e1b283f6c37b57f8238567b81c3db0f127f348f4842977'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Jul 2024 00:52:05 GMT
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
	-	`sha256:b1b3856af27e54cc3ed66b790bc96a5f11320ea8bddb38234094a40518eaf7c4`  
		Last Modified: Mon, 22 Jul 2024 21:00:01 GMT  
		Size: 14.1 MB (14071397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793002e3e156ffec624d53c95915201e7d170920d01cf1a2cf55e75a92874f1c`  
		Last Modified: Mon, 22 Jul 2024 21:00:04 GMT  
		Size: 211.6 MB (211637929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-7-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:e2285bd633e24bc992cc9c31eb1d987e7c943765975e75111a1fd1a1a49607a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8212348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314674b55ad9a698ec84602588e47481b83e7392423d28f35744d799c5d14342`

```dockerfile
```

-	Layers:
	-	`sha256:552c8402868bcae4dd880c5f44675779d7fbd84b9f164ff2c1f0327e544bbfdf`  
		Last Modified: Mon, 22 Jul 2024 21:00:01 GMT  
		Size: 8.2 MB (8193902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5800b0bb3e37cf688080d532bf612706029a508b53926431def617892ceb6c1`  
		Last Modified: Mon, 22 Jul 2024 21:00:01 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json
