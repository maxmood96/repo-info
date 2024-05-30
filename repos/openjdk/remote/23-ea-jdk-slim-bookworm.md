## `openjdk:23-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:cbaf54425f056f76d18be4d470ceab047fd5d918e8b0638b9f82584a56f494d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:8d37531e47603faba32327e6ac103c3607524d4406df79334a6f689d41aa0835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243616289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0f8fb2dd356ed2f7e24a976cc0ac902bda128738811dbb28c8ec38aeaa8686`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Fri, 24 May 2024 06:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 06:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 24 May 2024 06:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 May 2024 06:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 06:48:12 GMT
ENV JAVA_VERSION=23-ea+24
# Fri, 24 May 2024 06:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eebed7702933983781b97d468d8772f419c150d1c7354f82f15dd07d79be2b17'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ff14d6b86a66b88540ffd39b93e2e1ce8a529048d0ffbd3a5ff5b5dd14f8345'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 24 May 2024 06:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c94aee69c7909e01a524dbd5b0dbfda48972ab79cd587e461eede366480a02`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 3.8 MB (3821762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25073d4e583ebc49a9f78d28b70141593ea666bf036f95b03d8fbd89e3a4a4f0`  
		Last Modified: Wed, 29 May 2024 23:01:28 GMT  
		Size: 210.6 MB (210644116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:41f91926caa57daf9376e0a50d7d01018e47f314ccd39cb021c8dcbf3bd1bbcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1522124f78f59fcff1c32a9e4dd8df284fd4f02b40c8af20f80f76ef6f276afa`

```dockerfile
```

-	Layers:
	-	`sha256:b863dcc3161bde71111bb9de4bf7f857555873271c73178f8595e84114561e23`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 2.3 MB (2346317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1215d2803a0710d7d01f5250bef69c60fe9b93768201f44125d89dbf32f70a0`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 19.2 KB (19181 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6b64a40f273f087a0a244ed137feb4a4e75a6c2b0772c61c6454435178ada2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241346199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959cc931b5909678302c3b640e56eedafa757c72f16a1527f44ca2adc946e24e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Fri, 24 May 2024 06:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 06:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 24 May 2024 06:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 May 2024 06:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 06:48:12 GMT
ENV JAVA_VERSION=23-ea+24
# Fri, 24 May 2024 06:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eebed7702933983781b97d468d8772f419c150d1c7354f82f15dd07d79be2b17'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ff14d6b86a66b88540ffd39b93e2e1ce8a529048d0ffbd3a5ff5b5dd14f8345'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 24 May 2024 06:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0963731bbacd69f51ac2ab941acb3bccf110f4c9a6b6571eed17eb6612f90a10`  
		Last Modified: Thu, 30 May 2024 12:48:07 GMT  
		Size: 3.6 MB (3629849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b340e3fd7542e670b6a4c73b5c769b3c1559d8c08067d6d86d5fe71de5b76bd`  
		Last Modified: Thu, 30 May 2024 12:48:13 GMT  
		Size: 208.5 MB (208536847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:9ca82913a8044a4d5203f6067352d86c7d024323a722bfb278c1e4dd1b65c6b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1332d4b5d32df144bbf48eff43932db79f467dafd49088da6bdce9139229ed`

```dockerfile
```

-	Layers:
	-	`sha256:6124952f1e95c00ac6174a7d793039a8f000aa6aa7517244ab3d61751b143001`  
		Last Modified: Thu, 30 May 2024 12:48:06 GMT  
		Size: 2.3 MB (2346671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9a87356c8b2339cda3e008ff4e37ffeae190e7bc87182c7ad2fb1b06667ebf`  
		Last Modified: Thu, 30 May 2024 12:48:06 GMT  
		Size: 19.6 KB (19586 bytes)  
		MIME: application/vnd.in-toto+json
