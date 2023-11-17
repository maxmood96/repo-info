## `openjdk:22-ea-24-slim`

```console
$ docker pull openjdk@sha256:6200b8e822c39207971c2b27e1bff5b478b174a9fe99380f4f423ee032ddaaaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-24-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:a3ca9846aa2c2b1fc6cf87c797d638a3a815fe46e634d7f06c53606ebe352ecd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237786822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e723c87ed806b76715d1adde06e106eb54dbf9b5377497d7ff89100daac0c6e0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:50:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 11:50:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 01 Nov 2023 11:50:52 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 11:50:52 GMT
ENV LANG=C.UTF-8
# Fri, 17 Nov 2023 04:29:49 GMT
ENV JAVA_VERSION=22-ea+24
# Fri, 17 Nov 2023 04:30:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='f2b3d5371bc7ab762205f286fc5b5da9dabbdd0477965fc87d02076faf69ab3a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='909c2841030baff026a45248785f3dc50906ce921620913a28b8d6cca0075838'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 17 Nov 2023 04:30:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ccd98114e5f255102be6cfdbbef3e53c250ef2c03996832613a966d8943d1a`  
		Last Modified: Wed, 01 Nov 2023 11:53:11 GMT  
		Size: 4.0 MB (4017928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e607f00d393eb7e819c54b66b4779db214c3817b86b7d656e77bd7b425b9637`  
		Last Modified: Fri, 17 Nov 2023 04:33:35 GMT  
		Size: 204.6 MB (204619058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-24-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4671c0eb282e55ec789587c0a9db7aeba3ac7e0d97022493af50404efcc9d971
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235689952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c5d4d4e744388921332c9f47859f634507701a74dc5b271e4a41c560640bcf`
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
# Fri, 17 Nov 2023 02:06:08 GMT
ENV JAVA_VERSION=22-ea+24
# Fri, 17 Nov 2023 02:06:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='f2b3d5371bc7ab762205f286fc5b5da9dabbdd0477965fc87d02076faf69ab3a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/24/GPL/openjdk-22-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='909c2841030baff026a45248785f3dc50906ce921620913a28b8d6cca0075838'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 17 Nov 2023 02:06:35 GMT
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
	-	`sha256:9f9b521aada4ab295055707873658fc9ee6e85f8b589f3f94b6e00d4a85562e5`  
		Last Modified: Fri, 17 Nov 2023 02:09:59 GMT  
		Size: 202.7 MB (202686080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
