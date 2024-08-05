## `openjdk:24-jdk-bullseye`

```console
$ docker pull openjdk@sha256:32037318fbc60fecb384a751f42ef93f5c4df93c18fc68d938cc58a76e52e4af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:c59e8f4a159dd8ab04e7313edefb069c2371784235d45aa9d6f8bda4a54bcd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351342942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db26e67d1c044d61d42dc371c39b71548aabfe4265442ce54f0e0d473690bb79`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:08:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 02 Aug 2024 18:51:57 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:51:57 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_VERSION=24-ea+9
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='5dd8d67a4e4059d22eb6fe7c636bf7610832380061f522aec631b69fdbaba6ae'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef04b828af0fa6aca544841b01f5efda63143b81f52f1f69b2b5cf46953713a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8ed7043ae24342affc9e27ba2f362a3d02c164d6f2cc7b837f33b475f4ef54`  
		Last Modified: Tue, 23 Jul 2024 06:14:32 GMT  
		Size: 54.6 MB (54588538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d20f8eb5864215d130a7bb21beb1fbda3b535a74a42f8505b1996fabc6d807a`  
		Last Modified: Mon, 05 Aug 2024 18:57:56 GMT  
		Size: 14.1 MB (14071366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dc3bde4037c597084a33dfc223274a278a62347bea333ca76f41a30e32d16d`  
		Last Modified: Mon, 05 Aug 2024 18:57:59 GMT  
		Size: 211.8 MB (211834175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:6a8e4405611aa7256bf6bd09bda4970e041627a09ae27dc6e58e5c466a8ae499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8212348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c910e7319da58b01e0f2f38cdc9deea0ddf411401fbbd80c3156934bd8a8f8`

```dockerfile
```

-	Layers:
	-	`sha256:cc885439d30b2024aa98e1522a8aa4c98b70af3b41f441c4f74065e80b31d375`  
		Last Modified: Mon, 05 Aug 2024 18:57:56 GMT  
		Size: 8.2 MB (8193902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e44b86a016a732fed03715db2ed8439d752418c6b73442aae465a8f1b243fe8b`  
		Last Modified: Mon, 05 Aug 2024 18:57:56 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a45d5603fea715f41bf452c53b3a286a44cd8fbbbf3cc7cd65a1c39ddd0d7c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349406491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3089f0bdff891580e61f92a727339997da607da650f7b33fa85ed2a9623934`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 08:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 02 Aug 2024 18:51:57 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:51:57 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_VERSION=24-ea+9
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='5dd8d67a4e4059d22eb6fe7c636bf7610832380061f522aec631b69fdbaba6ae'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef04b828af0fa6aca544841b01f5efda63143b81f52f1f69b2b5cf46953713a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27a83c76abd51a72277b6a74eb7f88e560054e0d04383f64e2886877a20dd5`  
		Last Modified: Tue, 23 Jul 2024 08:11:04 GMT  
		Size: 15.7 MB (15749501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac540a55631c4cba93c7e4e4bf634300076d45e71db5f34f3c0d770eb826303`  
		Last Modified: Tue, 23 Jul 2024 08:11:17 GMT  
		Size: 54.7 MB (54694822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d2fc617cf24604b5fb20d3ed6e8d19726e946ac82ce538dc06fc0c823a93ca`  
		Last Modified: Mon, 29 Jul 2024 17:01:08 GMT  
		Size: 15.5 MB (15526258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fafb7fd8bb90cb704cba2c41f1506e71e838304bacbc6d9ba3d14b04188560a`  
		Last Modified: Mon, 05 Aug 2024 19:10:18 GMT  
		Size: 209.7 MB (209705923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:5a5c453f24c25a898d9397848c1a3a94be6e28c14018ef3c387c881fb3f56628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8314397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534fe95d83e19f8e9f72855fdfc646a5722ccde6853efff5fd2f7a1b83c10713`

```dockerfile
```

-	Layers:
	-	`sha256:36080ca0a0a27aa53a5863ed1c0014d0949a9e7a92c890b2270c967fd383ca87`  
		Last Modified: Mon, 05 Aug 2024 19:10:11 GMT  
		Size: 8.3 MB (8295612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc216ef9abb8e7778a156cc513aca6ba9b9b840d0938ba6788409d2f130ff55b`  
		Last Modified: Mon, 05 Aug 2024 19:10:11 GMT  
		Size: 18.8 KB (18785 bytes)  
		MIME: application/vnd.in-toto+json
