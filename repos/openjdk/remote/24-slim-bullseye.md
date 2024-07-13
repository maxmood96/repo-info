## `openjdk:24-slim-bullseye`

```console
$ docker pull openjdk@sha256:582e2a7ffbc27fb85d6be22f7976a3d2a1303fd4638025c61fcacfd00ad2b3f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:bd125fb364329df2ff85f355b8f84e7d62757fbd017e015b33a763a0c06bcab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244675184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05672faba12221314901e5f46ebde03331c60d86bb6f012cc3a4e5bc110f9770`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8974327ebe246a33a5f3e38e4c85b902514c707d06ddec52f334c1962fac8a16`  
		Last Modified: Fri, 12 Jul 2024 21:57:16 GMT  
		Size: 1.6 MB (1581821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a97811de5c97d806fa909dcc95a441e53c6313dc63d5afe884562ce3dd9680a`  
		Last Modified: Fri, 12 Jul 2024 21:57:19 GMT  
		Size: 211.7 MB (211671079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:bdd04621d370f877a5dc1323d5b31127e2265469bbeaa61cf8d47710495ddbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321e9b310b30466d465f10935915dd5937681ea0464b394d72b69dd0ba8b38f6`

```dockerfile
```

-	Layers:
	-	`sha256:5658cfbb02ec4941be3930653e5dd52c1a9c5647a7d58da8695af6264b8015a7`  
		Last Modified: Fri, 12 Jul 2024 21:57:16 GMT  
		Size: 2.6 MB (2638489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d3b81b82f493887830f778f52f0544f026e51bf1b1c00fa52b804d7c68e9de`  
		Last Modified: Fri, 12 Jul 2024 21:57:16 GMT  
		Size: 17.3 KB (17345 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e02962d45af2cb2cea45a7c230498830c51a906faff89985730be4ef9ad2588d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241186863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f09bdfa59a3f44662be705de6c308b4c3517439c6a4e8284dbd70d29cae7e56`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
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
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9481a8d2d3f3b38231f6c31bd2dc38c7c315578dd58eb8e02ef7320a34d44efa`  
		Last Modified: Fri, 12 Jul 2024 22:09:40 GMT  
		Size: 1.6 MB (1565925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91915aa680811fd58e58285af22c3d082a31690e58c6695452ec0d6b7fa7484c`  
		Last Modified: Fri, 12 Jul 2024 22:09:44 GMT  
		Size: 209.6 MB (209551323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:f88d99f17291d8ed9a1f509afda2511ba9bd057dfa4f286ab358cbd5c09aa803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2656443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400d24bc815c0833dc2bbb8d099e289d981f06352c09c68118d1fd289907689c`

```dockerfile
```

-	Layers:
	-	`sha256:a264b1d1af4d89886e3bd0032144892a7dd0e228dc697980b75856f72c1fa800`  
		Last Modified: Fri, 12 Jul 2024 22:09:40 GMT  
		Size: 2.6 MB (2638765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:041d8a5e4fe27e9c892e7650600ae3277ec5fff06e8a223bd0b5e75a3bba2ba4`  
		Last Modified: Fri, 12 Jul 2024 22:09:40 GMT  
		Size: 17.7 KB (17678 bytes)  
		MIME: application/vnd.in-toto+json
