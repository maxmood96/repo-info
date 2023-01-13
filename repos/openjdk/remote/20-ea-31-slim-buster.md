## `openjdk:20-ea-31-slim-buster`

```console
$ docker pull openjdk@sha256:d89cf44c18818edcb8943ce9b64f7c9f820ced20762d0cc8038991e9fde17a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-31-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:458d8dd22a3ea93d4b6f8b8f8c2cd38d355f87927509af9d093c386f93369b07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228936164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172520252449c56b1fd08890059298dbc41cedab50061ae6bbb15bc802b74d71`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 07:04:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 07:06:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Wed, 11 Jan 2023 07:06:17 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 07:06:17 GMT
ENV LANG=C.UTF-8
# Fri, 13 Jan 2023 00:31:35 GMT
ENV JAVA_VERSION=20-ea+31
# Fri, 13 Jan 2023 00:31:54 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/31/GPL/openjdk-20-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='3269ddcaa2745f47e0610531a0c6f06671f7b85fd4c02ae4a29a6f14089748a6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/31/GPL/openjdk-20-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ee53148820a0f603ef492aa7c62154c043cf38cea3259581a79010d8297c2f5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 Jan 2023 00:31:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828545e8b79db162ad5abac22f03044bd33fdec65ab2de0eab43a39483567a11`  
		Last Modified: Wed, 11 Jan 2023 07:12:21 GMT  
		Size: 3.3 MB (3275922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e448f4c2c649f14a6b87fe214471f2504c6a740948a45d6932159dad4ff368a`  
		Last Modified: Fri, 13 Jan 2023 00:42:01 GMT  
		Size: 198.5 MB (198519890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-31-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:effad331bde7a7a94b9fcbab61ab6c3c9c4718f225d466a7a5980f6254749dd9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226050972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676fe241c1f068ce4234d345bb867322571cfbe3f5aaf9b8782d0d6b28d21660`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:52 GMT
ADD file:08addf73dde8bf5ac64e0d9bdd1997ce5f406976c19da431616783c14fdb36ac in / 
# Wed, 11 Jan 2023 02:57:52 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 13:33:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 13:34:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Wed, 11 Jan 2023 13:34:43 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 13:34:43 GMT
ENV LANG=C.UTF-8
# Fri, 13 Jan 2023 00:51:18 GMT
ENV JAVA_VERSION=20-ea+31
# Fri, 13 Jan 2023 00:51:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/31/GPL/openjdk-20-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='3269ddcaa2745f47e0610531a0c6f06671f7b85fd4c02ae4a29a6f14089748a6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/31/GPL/openjdk-20-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ee53148820a0f603ef492aa7c62154c043cf38cea3259581a79010d8297c2f5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 Jan 2023 00:51:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7fac02f4cd2bcf681b9e156a67009cf4609f45447818b52327d93553bfeb2965`  
		Last Modified: Wed, 11 Jan 2023 03:01:58 GMT  
		Size: 25.9 MB (25914925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c3b6f956b3fce7c340f2d003d19d58e27ae60d033838d462212b60d5e10443`  
		Last Modified: Wed, 11 Jan 2023 13:40:37 GMT  
		Size: 3.1 MB (3129360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8be6e4c76662777ae93126ec413c46b9f0644b843a381e0d190b9d8af2007ff`  
		Last Modified: Fri, 13 Jan 2023 01:01:21 GMT  
		Size: 197.0 MB (197006687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
