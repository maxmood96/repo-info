## `openjdk:26-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:2950416389e8733bf5c697cf066dcad171f11f3c4b53a308e8d3c815a6b34dea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:bcdea72e2371c299b56a045b45f5e300d7c77e67ab54f5867762e3451a58af16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255458934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4493bd70b11f50972bf4689a4ee5b51ffe4a555f179a2776c7d767a4b7dd5765`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 Aug 2025 00:54:27 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 09 Aug 2025 00:54:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 Aug 2025 00:54:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 09 Aug 2025 00:54:27 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Aug 2025 00:54:27 GMT
ENV LANG=C.UTF-8
# Sat, 09 Aug 2025 00:54:27 GMT
ENV JAVA_VERSION=26-ea+10
# Sat, 09 Aug 2025 00:54:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='09044ebef2f1122e484e84df3a95605462c66caf6fb6363a6b3bb70cb6dba3db'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ffacf32c82e822c5ffb1400e05a279b08ddcc3f2c5538d01bf79f31c2af0fb2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 09 Aug 2025 00:54:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767ce3c4d69505b0f86acd26dff14094eb8103c269812833d8ce7a29d28b6ded`  
		Last Modified: Tue, 12 Aug 2025 21:28:14 GMT  
		Size: 4.0 MB (4027269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a06657b45e30469111fa18547ff0c3b997e814ff5885b9812fdea443372875e`  
		Last Modified: Wed, 13 Aug 2025 00:19:19 GMT  
		Size: 223.2 MB (223201410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:57d574ae4fdee87f996f567a00bcd497dea09c7eccd0f2f5e37412efd2acae85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2672147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2495a8fe494be74743d0fd69eaed10e3a22bb9dc6e18be70ac99f8d43881c44c`

```dockerfile
```

-	Layers:
	-	`sha256:3482fda8697529ae15f76b191027f04ed41d743cf3128ab65ed8fc375d2fa63d`  
		Last Modified: Wed, 13 Aug 2025 00:24:50 GMT  
		Size: 2.7 MB (2652705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75526d769fd16a43d5b58cf28fd6551fdd94e1b6f845072f480fca0db13302ee`  
		Last Modified: Wed, 13 Aug 2025 00:24:51 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:95406e69f87e4db7c182e8a0e403b15b555ab48caea2e4e5c949484612a83e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252944359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20579d359b1442ce4af4fbd3b07cddc98ad8bdf6daebe5ca9786c55827f8dc7f`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 Aug 2025 00:54:27 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 09 Aug 2025 00:54:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 Aug 2025 00:54:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 09 Aug 2025 00:54:27 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Aug 2025 00:54:27 GMT
ENV LANG=C.UTF-8
# Sat, 09 Aug 2025 00:54:27 GMT
ENV JAVA_VERSION=26-ea+10
# Sat, 09 Aug 2025 00:54:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='09044ebef2f1122e484e84df3a95605462c66caf6fb6363a6b3bb70cb6dba3db'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/10/GPL/openjdk-26-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='7ffacf32c82e822c5ffb1400e05a279b08ddcc3f2c5538d01bf79f31c2af0fb2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 09 Aug 2025 00:54:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9264d93e235056bbba86b53d5e1017f36cfe68b90a121050621f724be3d3805`  
		Last Modified: Wed, 13 Aug 2025 08:32:03 GMT  
		Size: 3.9 MB (3851294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd21e8fb90fa7ee1d3aece8da45bb424ea8722d9d8ef16336e791928a536a1f8`  
		Last Modified: Wed, 13 Aug 2025 16:51:46 GMT  
		Size: 221.0 MB (221011064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c71cb882608a7bdf8aa4a474b6eb1827e630852422247711121f176cb99336c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2668204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4faeb1fc37fd09ab73879214d1ca13835abe2db825416d05c41c634482e03d0e`

```dockerfile
```

-	Layers:
	-	`sha256:b6c374d15426513219a40a751484afdf73d5863798ad76463778bca31f1fef5d`  
		Last Modified: Wed, 13 Aug 2025 09:24:07 GMT  
		Size: 2.7 MB (2650491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:358ccc5388546497f3c0cd124fa9ed2c80e0938e2c70946529e047ecaa5b6fb6`  
		Last Modified: Wed, 13 Aug 2025 09:24:08 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
