## `openjdk:22-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:74db1734c556e84b728014f31df516e9f45332ded1e7eee751990949df877728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:f28f4255b082053bf5a3c922a8fd8c466d0ae8bd4f2a0ed93ed3e528f2773bd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239055634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1338ca9bd32e3eddac89630fd83ac7698cb386ae36cf20b8331e1c11940c1aa3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 02:48:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 02:48:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Thu, 12 Oct 2023 02:48:48 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 02:48:48 GMT
ENV LANG=C.UTF-8
# Sat, 28 Oct 2023 00:37:43 GMT
ENV JAVA_VERSION=22-ea+21
# Sat, 28 Oct 2023 00:37:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/21/GPL/openjdk-22-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='cefe6f9697801dd2a7abebdbd5b7bd36ad489794589e838562da46bde434ae5e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/21/GPL/openjdk-22-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='b77e7f170973c91690aa64a028f2e991828fde5092eabc29b602e26824216797'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 28 Oct 2023 00:37:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6b4e2c8e80e7a261b67542c6655d67269b5dad6ffbef15b5e49e5589289b82`  
		Last Modified: Thu, 12 Oct 2023 02:50:10 GMT  
		Size: 4.0 MB (4017876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618caab73a45ea5cc9841438a7f6723b47c2f7d6a193bfcd79edd154275c5188`  
		Last Modified: Sat, 28 Oct 2023 00:41:07 GMT  
		Size: 205.9 MB (205887884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9c7818cc53eecc86c82de6106c4e311b85cafa8917b0cf112e9f6d5ada2a9c51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 MB (237101486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395b93dad9a5257606e15166edc95eb239fe172a209def6aa4428194eb80932e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 03:22:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 03:22:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 01 Nov 2023 03:22:08 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:22:08 GMT
ENV LANG=C.UTF-8
# Wed, 01 Nov 2023 03:22:08 GMT
ENV JAVA_VERSION=22-ea+21
# Wed, 01 Nov 2023 03:22:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/21/GPL/openjdk-22-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='cefe6f9697801dd2a7abebdbd5b7bd36ad489794589e838562da46bde434ae5e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/21/GPL/openjdk-22-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='b77e7f170973c91690aa64a028f2e991828fde5092eabc29b602e26824216797'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 01 Nov 2023 03:22:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2dd8e8e8d27b55d70c431f7afee9699bc301524b9bc5acbea094fa677546b9`  
		Last Modified: Wed, 01 Nov 2023 03:24:14 GMT  
		Size: 3.8 MB (3824753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc1cfb9aa27edc072a6f3af78bf615ed2b9870c52d0d4e0b6d4e48dfb1bc2ff`  
		Last Modified: Wed, 01 Nov 2023 03:24:26 GMT  
		Size: 204.1 MB (204097614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
