## `openjdk:25-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:771be62721276ec6094dafabc31606dda33aa19801bb0f24286d1a0b7bcb1771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:942399b9d1366eb6f07db3419cdb95052ea9bc56591aeb460bba46dc6f82b5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245868346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac377ef0fd0926b310f4a9f212a168e24b0412e0334856c9575b5da2350edba3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 23 May 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='e47e49dfbb2ad32aa825a587f7aa6829a8ba6fac2b7f60d4cf5f38d8c5241c3e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a4306d6d5c87e8c33dc9a7cffa13b9c984f7173cc4921bce549781c5ada23cd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 May 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6ac79d0526b72cdc52d06c103f24942f814907ed43321409a99febf20ffe51`  
		Last Modified: Fri, 23 May 2025 19:55:12 GMT  
		Size: 1.6 MB (1583538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd5f4b96ac74fdf2cb775b113b11f99b64cf26767136b16dcbf45ca822df0bd`  
		Last Modified: Fri, 23 May 2025 19:55:15 GMT  
		Size: 214.0 MB (214028868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:0960fd2d1810eed9a38b920dfd61b145cd304fece04feb5ecfc3ab35207b7f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543f93c21212896e5b002c3fa3c3794a2e44a1d0be12805eda755464e2c6ff75`

```dockerfile
```

-	Layers:
	-	`sha256:3d0474824a12f4daf6c6fdf7d59d8fa43a396729b4eb87a5a96ff286059524a1`  
		Last Modified: Fri, 23 May 2025 19:55:12 GMT  
		Size: 2.8 MB (2848791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59662b01997c94d8b7ab81ac5e150a0a000b5cdc72a86403f54e261234a79f9`  
		Last Modified: Fri, 23 May 2025 19:55:12 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:04467d4cb2cd9f8b7d8652d78686c481519231c767ecd915b4e3df06bf8dfccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242120700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b39205a676554950cceebb3bf762d5cc2954850815cfd198bcc3bac6eb41d2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 23 May 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+24
# Fri, 23 May 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='e47e49dfbb2ad32aa825a587f7aa6829a8ba6fac2b7f60d4cf5f38d8c5241c3e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/24/GPL/openjdk-25-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a4306d6d5c87e8c33dc9a7cffa13b9c984f7173cc4921bce549781c5ada23cd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 May 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffa11c65fe0dd0f7246aa2d713287d4a2696818976b40e30107e62a132ee9e9`  
		Last Modified: Thu, 22 May 2025 03:35:17 GMT  
		Size: 1.6 MB (1567203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9289f4eb685a9dbf2fbe076991ab612bff39af169be1a17d6d02bb3a96fceae2`  
		Last Modified: Fri, 23 May 2025 20:10:24 GMT  
		Size: 211.8 MB (211807240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:2c973a4beaa814ec02b7c50c13306a95d6c0b77aa244de2b81d0a091966b1da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe4d8f32b46af8377edd934fd6b2975cafc410e54df31406ee199c0be8fd41c`

```dockerfile
```

-	Layers:
	-	`sha256:0d35df0f6293b8120b3f1ab7dabaf060f6d4c4d5c8b06caecbffc1a3f8f29b51`  
		Last Modified: Fri, 23 May 2025 20:10:19 GMT  
		Size: 2.8 MB (2848443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a3cb962b9c5877f7114a95cded346bad73419a8f6cf0a3897704d0cf82755ee`  
		Last Modified: Fri, 23 May 2025 20:10:18 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
