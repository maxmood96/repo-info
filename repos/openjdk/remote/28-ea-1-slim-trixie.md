## `openjdk:28-ea-1-slim-trixie`

```console
$ docker pull openjdk@sha256:76024d11b04329b04dfd521a6ca19843e3e9eb29ab158b186965ba7a691e99e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-1-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:0c7819640dc49afb31d647c7ca0d46bdc52bdd0ba4573047b15c51dabf17781a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.3 MB (259349143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02ed471e6bc5bff6c2be496643f6c411139d2c1f15d0148cadde5ee38945e35`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:47:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Thu, 11 Jun 2026 00:47:49 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:47:49 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:47:49 GMT
ENV JAVA_VERSION=28-ea+1
# Thu, 11 Jun 2026 00:47:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 11 Jun 2026 00:47:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0b65f7a36b6d538d8819e1e2a6c1e93dcef6426a887c5830d470f21492f655`  
		Last Modified: Thu, 11 Jun 2026 00:48:09 GMT  
		Size: 2.4 MB (2371286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ded5d52aee22ee69c23997a60c25d8a3c724760245d0e50b56125aa0dac073`  
		Last Modified: Thu, 11 Jun 2026 00:48:14 GMT  
		Size: 227.2 MB (227192442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-1-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:4bb12a10248467b3ec735692de497d15ec0233d9d7eba3f4360a3331aa7c8331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07488d7fcc615aff9674f59adf455509643b0097d1676608ba8fc1ce81dcae5`

```dockerfile
```

-	Layers:
	-	`sha256:03caebb0d5863dde5651137c1d859f5c695899608bd2cdc607e02d229bea009d`  
		Last Modified: Thu, 11 Jun 2026 00:48:08 GMT  
		Size: 2.3 MB (2276368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3691abf557c0ebfce772a14217c38fb0a7f46b0335ce16fb844a250ef736f2d`  
		Last Modified: Thu, 11 Jun 2026 00:48:08 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-1-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:216fc0f7e544793fd0a53afb8b7e3416aea3431715066bcb3652f46bacb9259a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257623712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2c2e5f62a393fa76db2afef03497299f7993da77890c3730881be938714f22`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:49:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:49:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Thu, 11 Jun 2026 00:49:22 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:49:22 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:49:22 GMT
ENV JAVA_VERSION=28-ea+1
# Thu, 11 Jun 2026 00:49:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 11 Jun 2026 00:49:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9cd2f70542117e7c6c05a7b6ee6a703253f40e3dd968045cf1a78cbba56b42`  
		Last Modified: Thu, 11 Jun 2026 00:49:42 GMT  
		Size: 2.3 MB (2314532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144db3498f47dd0baf5f9aed19bf86f9285164b2772603651b7008a353f34488`  
		Last Modified: Thu, 11 Jun 2026 00:49:47 GMT  
		Size: 225.2 MB (225160650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-1-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:485e4432465570a1892871dc14bf1958d98fd3d4dc694f0c71ff900c4af93582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3316d5734186892902c1611b469f92e5a96871b4a0b05f64afd96a43a4b5c64`

```dockerfile
```

-	Layers:
	-	`sha256:4274ba15837baaabf3518ea518b767f4efdbea739151d81a99d7333051996da5`  
		Last Modified: Thu, 11 Jun 2026 00:49:42 GMT  
		Size: 2.3 MB (2276046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e5bda6c46479bc82af195c34d81b63454137445caece464886ac2a9204feafa`  
		Last Modified: Thu, 11 Jun 2026 00:49:42 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
