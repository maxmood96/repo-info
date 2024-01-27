## `openjdk:23-ea-7-slim`

```console
$ docker pull openjdk@sha256:099680b14beca94fa9d4586378268fa141b4ee8d200a1e49f522ce213797c52b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-7-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:a3b48753e38403d8b714d73db6c36032ad9727c9851f69c026d2b9eb12b050ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236427454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7312213d2b461eb0865392a672aec0b06e5839ac5540e6edcfb0b899615953`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jan 2024 01:56:28 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:56:28 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='b10ac9dc80cf8dd508c44072989f1327a05a95dfcbf0af1fc65571ac2de613a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='b21ca578927851a80700167439bbb9cd75c7d60152d51240bac49be8dd548e7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5582a7fe399c9240dcdc77a85810160d26a45d4f0c072e7640d3f8c2a9ff92d7`  
		Last Modified: Fri, 26 Jan 2024 23:50:07 GMT  
		Size: 4.0 MB (4014811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529b8170499ac90157e98e77eb7108ecd5523b895f8d8d9a67ae2cfbb6cd526a`  
		Last Modified: Fri, 26 Jan 2024 23:50:10 GMT  
		Size: 203.3 MB (203286722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-7-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:7aee4a8b857b3a31ba285b957bd5fd7b8116cfcc937935b3736034a802d69fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c49891912830509f119cf71db88807e45e23663f417bcc1ad50c17c4661c606`

```dockerfile
```

-	Layers:
	-	`sha256:847aaae5d028cf077331dfbb69e90fe9d309f456901ae38d6594e50c808f6c14`  
		Last Modified: Fri, 26 Jan 2024 23:50:07 GMT  
		Size: 2.0 MB (2037175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:631c87f81556b6e941f2be08c10de7031621082179a1dbd4fa521cec706ddf08`  
		Last Modified: Fri, 26 Jan 2024 23:50:07 GMT  
		Size: 19.3 KB (19327 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-7-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:177cfb10bcbcdf25e0b7b002502d35cdc18758f3ebe971fd0a773d70c8477f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234164762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f302e0f70f6768c55691ab60083d8eae96b61385c66fead254421a34f24d60`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 26 Jan 2024 01:56:28 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:56:28 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jan 2024 01:56:28 GMT
ENV JAVA_VERSION=23-ea+7
# Fri, 26 Jan 2024 01:56:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='b10ac9dc80cf8dd508c44072989f1327a05a95dfcbf0af1fc65571ac2de613a7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/7/GPL/openjdk-23-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='b21ca578927851a80700167439bbb9cd75c7d60152d51240bac49be8dd548e7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:56:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0a57d63de2128216c0a50f93a2c6c345b1a3ab26c76b45d6d31cbe4f094fde`  
		Last Modified: Sat, 27 Jan 2024 20:35:57 GMT  
		Size: 3.8 MB (3819893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc63c6f952f8acd0cace62f43d0f5e92e1877a9d19e14083f7112764b0e3ea7`  
		Last Modified: Sat, 27 Jan 2024 20:36:01 GMT  
		Size: 201.2 MB (201187534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-7-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:437551da85c4b961a9b4e2aa015faa2dc2ce1b37ffdd614747197eb039885784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2055739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc393b9440563e1af7121082dc60777c7d84fe1f650794cac6d013fa6788d0dd`

```dockerfile
```

-	Layers:
	-	`sha256:d24e8d5c43b5780765883c0dc018397fcb43d42ac31ba3fc3a7b5b2e02f00b62`  
		Last Modified: Sat, 27 Jan 2024 20:35:57 GMT  
		Size: 2.0 MB (2036553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d012f0a758bae26ab1c433803ae01ce90dc08fce937461fc0403af315a389e9e`  
		Last Modified: Sat, 27 Jan 2024 20:35:56 GMT  
		Size: 19.2 KB (19186 bytes)  
		MIME: application/vnd.in-toto+json
