## `openjdk:23-ea-29-bullseye`

```console
$ docker pull openjdk@sha256:73c0477c3ce2c2d60c764d5ce68011bb8591614ffeb5a60e6d4fee5ad455ad93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-29-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:5dc82dd05afde79d40a416309cc9d32e754bdecb5233b16b7342df03abb32f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350917889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651ce2b09414892bd6f5480799107d9f352b28078a30127b6b7cd8c8b96bd86c`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 29 Jun 2024 00:48:10 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Sat, 29 Jun 2024 00:48:10 GMT
CMD ["bash"]
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 29 Jun 2024 00:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:48:10 GMT
ENV JAVA_VERSION=23-ea+29
# Sat, 29 Jun 2024 00:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='1ecb4977a7385dde5f7155e22cfdad0bec51afb8ff4dece08a061bab64be8aaa'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/29/GPL/openjdk-23-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='a14bddc20e706cf85f28b8cc360e3dc2506b51cff9a0e62125f3213de6c41f00'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:48:10 GMT
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
	-	`sha256:3fc3d6a7b7e8cdd57b0315885921e7660992551d165db338c30a88e8f9c32893`  
		Last Modified: Tue, 02 Jul 2024 03:21:26 GMT  
		Size: 14.1 MB (14071326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f998b87e42b62489e86a09981773b5d2e60b2363c672f5ef4d2faeda0a3756fd`  
		Last Modified: Tue, 02 Jul 2024 03:21:29 GMT  
		Size: 211.4 MB (211412392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-29-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:0f56fcb544bf0fde284e925eaa3400fc620f7515a0ac1183303d2cb6773d0bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8175823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda795911a1a749eb6b0270c0a37bfe9dd40b3044b7312a483d818852b7eb404`

```dockerfile
```

-	Layers:
	-	`sha256:ec70a2d7ef0f0c992db65620de75ee28e2ae9be81d62bca173d2ae30d982995f`  
		Last Modified: Tue, 02 Jul 2024 03:21:26 GMT  
		Size: 8.2 MB (8157360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a9c5c638ed4a0a861608ee55106c33ff786b5ec19a9723e74daaa10833091d`  
		Last Modified: Tue, 02 Jul 2024 03:21:26 GMT  
		Size: 18.5 KB (18463 bytes)  
		MIME: application/vnd.in-toto+json
