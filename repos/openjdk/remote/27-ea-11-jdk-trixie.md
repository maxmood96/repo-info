## `openjdk:27-ea-11-jdk-trixie`

```console
$ docker pull openjdk@sha256:57445af9f236a87388663dd42b933376f4b7c2b61b86cb439101514fdc22eecb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-11-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:509761d0acf23c706c3a94d53d4b55a7d39ca442ff45500c794507dc84cd1260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.3 MB (387289199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d5c87063f704fbcd9a77c0f8bc4a243dda1f449195b2b3631856cf866cf3bb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 02 Mar 2026 21:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 21:25:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 02 Mar 2026 21:25:20 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 21:25:20 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 21:25:20 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:25:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='75a300b52539589c8c4b172ef292d5b58486de4d88d774be659975bc661767bf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='3bf27bc49545e677311a0eab8a838953f4726191499accef492c7feaf801e429'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Mar 2026 21:25:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed881fbf1b07b42dd470cd5b56a8feb684d60879c6f8028a9e7a8715e0e72361`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 25.6 MB (25614562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da421ddeb655bdfb3960e490b39373b0d1351e3eaba61d01978107920638392`  
		Last Modified: Tue, 24 Feb 2026 20:04:27 GMT  
		Size: 67.8 MB (67778971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951556ee197b3ed0d13f4c5831ff30c9ba9aefa975106f8e503fcaf21bb9bd65`  
		Last Modified: Mon, 02 Mar 2026 21:25:45 GMT  
		Size: 16.1 MB (16062947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b66c540966c1ff74b55928f5c0b490f95e3b79ba62ac9c12f57057c5923f6`  
		Last Modified: Mon, 02 Mar 2026 21:25:48 GMT  
		Size: 228.5 MB (228539595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-11-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:522fd8ea77453c9c508cd92dd95f61b80103e6b7964b056eb534ec0d84aafdf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8528937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a64b8d33f29ef473433756ddbd318ec08050df0fdd458d5e1e68266ec810ea8`

```dockerfile
```

-	Layers:
	-	`sha256:0940ddd18bbb416f713ce9ff3cd9b7595039d656d28b39e0410bf47bbe56637e`  
		Last Modified: Mon, 02 Mar 2026 21:25:44 GMT  
		Size: 8.5 MB (8511024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb447d72cfb66e295b0e0ce5981f215b5ec8b975d16318615d677f5754e18bae`  
		Last Modified: Mon, 02 Mar 2026 21:25:44 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-11-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dc7bde60c95b1b800fb4e6bee93a8ada8d891c4d747bcba442e9bc7d15fdb460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.8 MB (384820691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499b47b72ba5e036c3652e2fecb73658416bbb8c4d2e94a1c419a1e4d8a4b122`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 02 Mar 2026 21:24:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 21:24:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 02 Mar 2026 21:24:36 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 21:24:36 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 21:24:36 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:24:36 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='75a300b52539589c8c4b172ef292d5b58486de4d88d774be659975bc661767bf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='3bf27bc49545e677311a0eab8a838953f4726191499accef492c7feaf801e429'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Mar 2026 21:24:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da832d1713c4ed161275cd40c4161680fbdd97c6faf23e71654d26bb2e58d6`  
		Last Modified: Tue, 24 Feb 2026 19:25:09 GMT  
		Size: 25.0 MB (25023493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c46eec5989abc098640d80ee9b97658d4487864f3268219dadc63c0a047866`  
		Last Modified: Tue, 24 Feb 2026 20:15:09 GMT  
		Size: 67.6 MB (67585551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559743683b8ba27b7c18a22a70d6d87f356590a16cdc8f4ddb3e799adff43ffe`  
		Last Modified: Mon, 02 Mar 2026 21:25:01 GMT  
		Size: 16.1 MB (16071574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c3d1f5890c848e46c680e60a5136585407d46f541e850aeb8af3f15a995829`  
		Last Modified: Mon, 02 Mar 2026 21:25:07 GMT  
		Size: 226.5 MB (226487905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-11-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:552d7298e01092c98f34177199cceaa49fcabfb9e9b79cccd3e50de3fe24aaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8723846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c082bb0c2005ed76a945abdd9a246d007b0daefab5773ec47618e08af4d98a16`

```dockerfile
```

-	Layers:
	-	`sha256:dfe915f12bb803a365f517d9a81a9beafdc7c6aaee4c588dff90dd1600997b08`  
		Last Modified: Mon, 02 Mar 2026 21:25:01 GMT  
		Size: 8.7 MB (8705814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45d8eec0ed7ad25943c19e41dcc42f8ce406ba6f5838960df9260791ad4a674b`  
		Last Modified: Mon, 02 Mar 2026 21:25:01 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
