## `openjdk:24-ea-12-bookworm`

```console
$ docker pull openjdk@sha256:fc8ec109665988339a36ba8d9b754036ab7096cfe82e9dfffaa8d78dcb398c53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-12-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:a5afe493af665c5f57b35057d4eaa6d6156519dfb806e53a99da12de2021704f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366651880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d42c2508374ebd2ffb3a60ff8d2ce53b9a8beb7e1ac34dd6b68257e0a4cd4d1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:09 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Tue, 13 Aug 2024 00:20:09 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:43:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Aug 2024 00:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 Aug 2024 00:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 23 Aug 2024 00:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Aug 2024 00:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 23 Aug 2024 00:48:14 GMT
ENV JAVA_VERSION=24-ea+12
# Fri, 23 Aug 2024 00:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/12/GPL/openjdk-24-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='9a859e4f3840e3f0890051a26b06413cd18dc8a1b7d68b221f47b38ba2f5add4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/12/GPL/openjdk-24-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='4631ab62c58dbecfc00983df819c9a669b3d4fb681d7f6c3d95af11b7aacf087'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Aug 2024 00:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed93aa58a52c9abc1ee472f1ac74b73d3adcccc2c30744498fd5f14f3f5d22c`  
		Last Modified: Tue, 13 Aug 2024 00:50:05 GMT  
		Size: 64.1 MB (64143347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bbbf33e644ffe02865e9cc067eec4d3d5541b45183a344158a28a131e7ae8e`  
		Last Modified: Fri, 23 Aug 2024 21:11:00 GMT  
		Size: 16.9 MB (16942982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ea37a443e427112598538d0a55c6e21108a72cc7eeeba98613391ee409d920`  
		Last Modified: Fri, 23 Aug 2024 21:11:02 GMT  
		Size: 212.0 MB (211960774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-12-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a067a6965beda05a887beedf6fb66dd91c47be11fd6e77cadf8d18fa221266cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8276457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f80728c67ba79598de6e1801835b92500b59c813c844ee935610cd43f8d6f77`

```dockerfile
```

-	Layers:
	-	`sha256:5d49d989d4897b0f1b8a73d1d4acd6316abf1fcef3f6f607a65338e4dda31bf5`  
		Last Modified: Fri, 23 Aug 2024 21:10:59 GMT  
		Size: 8.3 MB (8257994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:540713a4cb77e73b9730fd05a9ed99b242bd1932bdcc9c936f12659be28dcac8`  
		Last Modified: Fri, 23 Aug 2024 21:10:59 GMT  
		Size: 18.5 KB (18463 bytes)  
		MIME: application/vnd.in-toto+json
