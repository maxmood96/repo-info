## `openjdk:24-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:24321d728fc0d9eddd29c93ee08af818d2ddcd5bf68af767b1a6222ef2f08d2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:01e541be73d6046ca2e2e7fd272cb791bf7c381a543f62790e6f8d19cab2f341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244839280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67b0fbc86eea3028b4a460424b61301d3ad0cfb5d343e5a767d477cff817ae8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 00:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 20 Jul 2024 00:52:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 20 Jul 2024 00:52:05 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 00:52:05 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jul 2024 00:52:05 GMT
ENV JAVA_VERSION=24-ea+7
# Sat, 20 Jul 2024 00:52:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='d175c4cfc7ab8306b42cf88fe0e60b2b827a2106c026ae6d2a3f2e51bbcb60d0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='5df46f7b64a38a7a34e1b283f6c37b57f8238567b81c3db0f127f348f4842977'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Jul 2024 00:52:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fef15283823fe18a10fdbc179a5fd89a419130163bf7a294632b20f4ca371e`  
		Last Modified: Mon, 22 Jul 2024 20:59:53 GMT  
		Size: 4.0 MB (4016755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8708c7a53d682dcd214a279506814a3de13a0791f80f669469d2cbed7b79c008`  
		Last Modified: Mon, 22 Jul 2024 20:59:55 GMT  
		Size: 211.7 MB (211696247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:18ddb6a1c66a3b69b83cd6b70aca69525ab1350392197e2c81125ba015fb9822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38eb8c5e90d78e5fc408eacf3253c462d1a0743630ec1cb71be144aa2410d1c8`

```dockerfile
```

-	Layers:
	-	`sha256:24d2447f73f1026d196950ddc7be81ce1328e61920271ecf8d92f5f745ca0f0e`  
		Last Modified: Mon, 22 Jul 2024 20:59:52 GMT  
		Size: 2.4 MB (2365294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017fb65b13b85184d3ffb95a9e1b606974cf043ccc6a77c11ed46789d900eb76`  
		Last Modified: Mon, 22 Jul 2024 20:59:52 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c33d72a38980d750572a3a9eb27ce6c1c59f2a64976ab27b8b84cf1e8719e021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242541655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d1712e6bec8d19a646fc172bc1855eef5cfdcb94fb339b3c39976d3ed31226`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 12 Jul 2024 06:52:24 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_VERSION=24-ea+6
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='85969884f11f2863595c13dff1cb6f6d94149bbe5188c34f0a7aaa284a545a27'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c719648382b7e5d564dc1d39d4408890d92ce5484fd46a5ef338da7380684ca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0370b31cbe4825d7532c88b6301fd41a3b91f7ca9bfeb28d0c0a0d92748ce685`  
		Last Modified: Fri, 12 Jul 2024 22:07:40 GMT  
		Size: 3.8 MB (3829944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63db856f7319c0e6bf8faaedfc24d3f2b18dd1ccc01dab5f20d05bc020caea5a`  
		Last Modified: Fri, 12 Jul 2024 22:07:44 GMT  
		Size: 209.6 MB (209555148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:afdab6a1aeb5a6500c57a53476778d4674a167b404a5064c7a0a14be204e3445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f03834272ce9c176caad9db8c0ec873f3d0e3039d9a83b7ad80cc6d61c1810`

```dockerfile
```

-	Layers:
	-	`sha256:785f3418e775f810882550be1a9b6f0e790fa5f704c2ef3c9c066380b32ac32c`  
		Last Modified: Fri, 12 Jul 2024 22:07:40 GMT  
		Size: 2.3 MB (2346687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:493e255335fc8540c49be7bed01f3cfe603a21427fd238e1a21861ce31e6137c`  
		Last Modified: Fri, 12 Jul 2024 22:07:39 GMT  
		Size: 19.6 KB (19618 bytes)  
		MIME: application/vnd.in-toto+json
