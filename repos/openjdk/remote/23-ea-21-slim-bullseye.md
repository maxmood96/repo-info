## `openjdk:23-ea-21-slim-bullseye`

```console
$ docker pull openjdk@sha256:e84f0ce753e622d2d655b5982022c8b854525db7ea940cb90818378964ef878e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-21-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:8e2905cc59f5b181ae4153a248a65857dab672dd2ecb6fa0da0c500821ca3605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242843037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f09162803618214c9f1ab8f43d996e390cfa9aafc4d048497103834175e014`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 03 May 2024 00:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 May 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+21
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='20f3d065d5757feeac026eba758dd431f1343b5087c7f0f03ef8bbd2fa606bd4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='33a4798e59e479514004a62ec1863207430915212696689ea072cd7ad0b5d15c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 May 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7555dbfdf08f7df05da130a251b68f04aa5d2b32705d6b7e89a6ffe63a2599c`  
		Last Modified: Mon, 06 May 2024 23:05:40 GMT  
		Size: 1.4 MB (1378039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c491768ca30c46b648afb81dd29a1d766e54bd82b1a8cb54224ab1de1bea0fa`  
		Last Modified: Mon, 06 May 2024 23:05:44 GMT  
		Size: 210.0 MB (210030735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-21-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:786140a18ff611a809184407e303999699469a68af1a7f3d91da82bf40821cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce3a72013bb5a625f2708d424c841688b531ea344c4980be0474cfbda835ee6`

```dockerfile
```

-	Layers:
	-	`sha256:088e37f45cb56986fa4bc52ea9a1d1716459b440f83f03b16a060879c0569e5b`  
		Last Modified: Mon, 06 May 2024 23:05:40 GMT  
		Size: 2.6 MB (2638489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc1081ed06422e6667b4bbd4fbc5526b30d119d3e1f7eb2b54f0228d1f623811`  
		Last Modified: Mon, 06 May 2024 23:05:39 GMT  
		Size: 17.5 KB (17476 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-21-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d5ad97c6ac377f6bc8acd6412317233687f2d5e61e55fa7a77549426c31c93af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239363444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa97a96843f25e9f6394a336c8f18b226ceb2f3c232034f87a171662365ac2e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 03 May 2024 00:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 May 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+21
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='20f3d065d5757feeac026eba758dd431f1343b5087c7f0f03ef8bbd2fa606bd4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='33a4798e59e479514004a62ec1863207430915212696689ea072cd7ad0b5d15c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 May 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e1ff5972418c28862eebf600ebc7f9f20a7a6d5c18d60f7e1147fadcb3547`  
		Last Modified: Tue, 07 May 2024 00:23:12 GMT  
		Size: 1.4 MB (1361947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfb282cd1751f4d0c9520a7204595a2d5e0b95678d5f9bf5af5e41a67992cd3`  
		Last Modified: Tue, 07 May 2024 00:23:16 GMT  
		Size: 207.9 MB (207914161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-21-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:66e93720f2dd8d424614e1465f42f13a1fe6a2c63b382c0e834651b974d1cd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2656023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2d7a94fa5f6ecd36645db111e877e747240b3b94f49ff491592096b9e591f8`

```dockerfile
```

-	Layers:
	-	`sha256:68d8643e29b02c154d4f4f3d14e9a334e7e860f7b215d85963ef10b78cc985d7`  
		Last Modified: Tue, 07 May 2024 00:23:12 GMT  
		Size: 2.6 MB (2638700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7995e93b34834db025bdb17ee85215bddffba472c24a9a83458b1d85753604b`  
		Last Modified: Tue, 07 May 2024 00:23:12 GMT  
		Size: 17.3 KB (17323 bytes)  
		MIME: application/vnd.in-toto+json
