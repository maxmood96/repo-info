## `openjdk:22-ea-33-bullseye`

```console
$ docker pull openjdk@sha256:f0b3552ae7e3abdd7e34fa11fc0fa50247435b41e2896a883665085dad2d936c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-33-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:d9154b9a8e234c8016c6a54dad7a72ab7cb92b1f0f390b0dee2ba27020f5ecc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342371403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b552b19f6beba1e72090df743ca73b06f42ee851a8eebf8a72f85f3853bba6d5`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:36:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:32:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 26 Jan 2024 01:48:32 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:48:32 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_VERSION=22-ea+33
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='585ce01cf4908a98290ff33cc072d8733a012a58cb13a25304904bdb03c5e751'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='1df9746a0ac9f82fa421e32e0eaa4347dd657d612ca3e414c50b7e689ad59b43'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24098c8d74fae9a314e70517566e785db7b39341cbc4bd63adf14c330728677c`  
		Last Modified: Wed, 17 Jan 2024 02:01:11 GMT  
		Size: 54.6 MB (54601537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a75c971c7c7568b147cd9db6b70721cb93fbb6c35c12cc467772fa728422e44`  
		Last Modified: Fri, 26 Jan 2024 23:50:14 GMT  
		Size: 14.1 MB (14073015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68381b52a57eaec8aa47152031488f875ba00fb9bd523e9a7e6cf0aad600e4d1`  
		Last Modified: Fri, 26 Jan 2024 23:50:17 GMT  
		Size: 202.9 MB (202874015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-33-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:b51d10030b20242108fef75af7b771ccb5ce0872f06a9c8802e67a97945cc274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6974990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42fe28d87b3b70e5a2860b552f350669ab65e409faf9fa75af98b43deb0543ec`

```dockerfile
```

-	Layers:
	-	`sha256:c67cfc3a50cad22867ecd92ade5d07724823d08e77b880296b2624b6574f972f`  
		Last Modified: Fri, 26 Jan 2024 23:50:14 GMT  
		Size: 7.0 MB (6956084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2213d6dc56e5fa57d49fd03b648ea58dabf9019e6ecd0a7bacf5c23b353fdd2b`  
		Last Modified: Fri, 26 Jan 2024 23:50:14 GMT  
		Size: 18.9 KB (18906 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-33-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a8c80a722a9b0b89f10d9926ededb1a32f8d05890707e97cce25bf715aa136ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340614942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611df5be8fb0500045536d7c864e25ee30c5d0029e2e1f95dc51c2d4d7980b82`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 26 Jan 2024 01:48:32 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:48:32 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_VERSION=22-ea+33
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='585ce01cf4908a98290ff33cc072d8733a012a58cb13a25304904bdb03c5e751'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='1df9746a0ac9f82fa421e32e0eaa4347dd657d612ca3e414c50b7e689ad59b43'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebf2a961043d6b9dd703d0a485e216a2e302edf2e2525f7f410987d26905e71`  
		Last Modified: Thu, 11 Jan 2024 09:35:03 GMT  
		Size: 15.8 MB (15750711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646806c0e22a1bfa60edc42bcc6170f0ccd02431e5871b9cec1962c34d610232`  
		Last Modified: Wed, 17 Jan 2024 02:59:33 GMT  
		Size: 54.7 MB (54699826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dead6015bbcc859ea7747d32a4e7cab2e3cbe04c839563c1a7d519f9e82d7483`  
		Last Modified: Sat, 27 Jan 2024 20:36:57 GMT  
		Size: 15.5 MB (15527320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91af74f90bade88370fbcb7d8e0578d9debdabe0174448f9da762b784fd915cb`  
		Last Modified: Sat, 27 Jan 2024 21:17:29 GMT  
		Size: 200.9 MB (200929238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-33-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:bcb91b6579dab8db380b40555907a6c84c50047143338bb052683c55206e9aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce18c86d9de8190ba02ef54de21df6ee04eebd1bd26d4ff89be949b569fe529`

```dockerfile
```

-	Layers:
	-	`sha256:e7b78f5fb3fa60f63f18d8313b47b95389a6f72e41d0b4072629981021caa516`  
		Last Modified: Sat, 27 Jan 2024 21:17:23 GMT  
		Size: 7.0 MB (7043732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8c3cb0851b8b9c1f29d5cf7dd61894029daa47f972cddb61e64b9dad8b5c55`  
		Last Modified: Sat, 27 Jan 2024 21:17:23 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
