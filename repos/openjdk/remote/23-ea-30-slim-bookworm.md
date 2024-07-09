## `openjdk:23-ea-30-slim-bookworm`

```console
$ docker pull openjdk@sha256:6133845f04fd416e8e7c4dfcf179cf7054732a75de384ca14baf13d7e5288d66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-30-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:fee12c790d842b64e5648c6356cacbf54925b5ed454f1876747b438afea71576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244621741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f33372da0bb471f5c2fe89dafbd99ae6511cb4c051584deb593e9bf3ed2e51`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 06 Jul 2024 00:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+30
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='847f053c0a1e23b388353fdfa7c43ebe7eae98f8221e43d561a0ad3a4c486681'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef0255786108e95110839309fe5ed09fc730c0e3d78dd3d84d3f0f7e520a0d93'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990b4d201c5e45b0a0436dbc39279a21a501e2292ef9199f4cf612a0e02947da`  
		Last Modified: Mon, 08 Jul 2024 20:57:09 GMT  
		Size: 4.0 MB (4016805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb6b2b0615589495a30950471e62a0b30169c19a1e7943645e0735e9850faff`  
		Last Modified: Mon, 08 Jul 2024 20:57:12 GMT  
		Size: 211.5 MB (211478658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-30-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f76ef506b70fb926ecb46fbf80a80c867661c7e92762d403580c17d16af6ec35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f0442e47bc88eca87711ecefcab32f7bcc6e428a842f37551f8805a74f4e06`

```dockerfile
```

-	Layers:
	-	`sha256:a16a535835b2c7756bf9dcc435542b14585332a92738180ad0abf103b8360af7`  
		Last Modified: Mon, 08 Jul 2024 20:57:09 GMT  
		Size: 2.3 MB (2346345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd2ed739a82ffd4b488679a52263838985a33d11be520b641a4e7b4530115eb`  
		Last Modified: Mon, 08 Jul 2024 20:57:09 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-30-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a586e93ea7a7b5549d194891da681a4a1cdecf876268e2e2d0be8188c83d1304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242328318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fcd8be1cb8179ba75a148c986c9016721c67de3478918e27b3e6880044fae28`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 06 Jul 2024 00:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+30
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='847f053c0a1e23b388353fdfa7c43ebe7eae98f8221e43d561a0ad3a4c486681'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef0255786108e95110839309fe5ed09fc730c0e3d78dd3d84d3f0f7e520a0d93'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2149aac5fc65027f104f3e2bd5589eb7f7ac9175a7e33784da9a9f11041f05e8`  
		Last Modified: Mon, 08 Jul 2024 21:00:06 GMT  
		Size: 3.8 MB (3829946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7910d00517979fc087ef5795938878f2cbbb337bb7bc8cd09a132763c8f5f505`  
		Last Modified: Mon, 08 Jul 2024 21:05:43 GMT  
		Size: 209.3 MB (209341809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-30-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d1e20c72283dd49a121061989c25509805e9206adde67648c3d2fa965e6d70bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafa198c5512f1afcb17f8422d9b9f3c84dae9bd7ec57b186cf1828c86c2605a`

```dockerfile
```

-	Layers:
	-	`sha256:d479e12fe82ab0cbdc277c7fe20deadd61019315d497fd05ce89c87ddbfa9412`  
		Last Modified: Mon, 08 Jul 2024 21:05:38 GMT  
		Size: 2.3 MB (2346699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aaa787e5c8122de3d294c15e5265e8bb818f889be4b1d49e09e67ce500e2bae`  
		Last Modified: Mon, 08 Jul 2024 21:05:38 GMT  
		Size: 19.6 KB (19635 bytes)  
		MIME: application/vnd.in-toto+json
