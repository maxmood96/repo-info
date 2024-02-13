## `openjdk:22-rc-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:18460e1a2da5fe54f387327e67bb0961e5b2d99e0ca7c2d43ae298b836dd82d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-rc-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:14f862b50b07c46dfb87dc7391c6d8aeeee197348624acd136ee2264d16d1f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235930482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6deed4ab8c6337abaf2ba3cefb1ed959d64dceab91cd86e9793e312813491a0d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Feb 2024 19:48:12 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["bash"]
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 09 Feb 2024 19:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_VERSION=22
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='37b0e1d93e9b6478824c21753f2e8445c8caad885a2245f393b35658be1695b3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='5bc8c3ea634bf3be8a275c789dabbaa3e68eb639ee920b6fbce1b2236082086d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9715287ade6cfbddb9a715c7f684573752b0311f7349c6ee2458a6783dbf0090`  
		Last Modified: Tue, 13 Feb 2024 01:53:49 GMT  
		Size: 1.6 MB (1581868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85b1002ff83164cfe5e11fe87e03328f6ba2e37ebe7517b2a69f3d0c9632593`  
		Last Modified: Tue, 13 Feb 2024 01:53:52 GMT  
		Size: 202.9 MB (202926189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:d53e0cb9558458f5a243824c28cc0ab2adfb37a44cd48eeee2949f10cdaf4fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d400ba85581a683208aaf4125379c76fd8f0ffcecf7900f430b77ab154a46e`

```dockerfile
```

-	Layers:
	-	`sha256:2ffcaf1ff9cdb9efd2635892ab6bdf6750c3667260c16243d04c31272adde83b`  
		Last Modified: Tue, 13 Feb 2024 01:53:49 GMT  
		Size: 2.3 MB (2281278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27eb5ed5dc426ba2417e9a04b9588f9813a80073fb975e3970b9d974db043454`  
		Last Modified: Tue, 13 Feb 2024 01:53:49 GMT  
		Size: 16.9 KB (16867 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-rc-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1c8f4605bcfc8f3416f615416a062f7e4272dd947b0a901cafec602cb38ecf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232406919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1d70b0cd6a85007b68ae41946b5b168cb3efb2f8484878769634ceeaa20a61`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 09 Feb 2024 19:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_VERSION=22
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='37b0e1d93e9b6478824c21753f2e8445c8caad885a2245f393b35658be1695b3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='5bc8c3ea634bf3be8a275c789dabbaa3e68eb639ee920b6fbce1b2236082086d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3bc7f554a0ea1458559926cfeb111c558c33065ef21aaaadc2eb1182f2acd0`  
		Last Modified: Thu, 01 Feb 2024 16:21:04 GMT  
		Size: 1.4 MB (1361927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b74ee7c4dddbf9cf9b2c5bd6e9c13bf29841c5dc92a5ca627a7a6368b184c5`  
		Last Modified: Tue, 13 Feb 2024 00:35:30 GMT  
		Size: 201.0 MB (200980658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:6c1510ec7a8ae80c8e1d6765e316e31ba085831ee654c8441cf8c7e8cf373533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa86773aa1f34368b3cacaa61ad24a8b830cb4ae11bbe209fd42c03e2e006c27`

```dockerfile
```

-	Layers:
	-	`sha256:3bb7219a3ba49170d1f9f2ea5b202801783a56291149da063576380832c7eff9`  
		Last Modified: Tue, 13 Feb 2024 00:35:25 GMT  
		Size: 2.2 MB (2189827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06d6b7397d832d2f337fcc87a887dbea423f5eff50e6dca1d11d0bb16aa64b4c`  
		Last Modified: Tue, 13 Feb 2024 00:35:25 GMT  
		Size: 16.7 KB (16711 bytes)  
		MIME: application/vnd.in-toto+json
