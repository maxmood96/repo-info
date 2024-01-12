## `openjdk:23-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:c84fe3e6634f71a9d64b27de86465b487b8f6327e0455084bd46adec6fee242e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:14936b82be6be492d1bd026b6661da7426b4c1003b9c18f4de0cb9f996b82720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235957024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5140b488ffa186a1a8f0b9dce172ba2f2389c8301cac55cb24dc63dfc210db`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 06 Jan 2024 01:52:17 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Sat, 06 Jan 2024 01:52:17 GMT
CMD ["bash"]
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 06 Jan 2024 01:52:17 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_VERSION=23-ea+4
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='9a68dc2301a1ab9d674095ba14205b79ba23dd83002077ae6777edc820e789d3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a7293d34fcb6c1b9f5b0bfc74aabc4e695b0e6d6b6778172d59596b19db6e4e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d47bbcd2cf468b96652e21696798c052b4f7c83f25ac0b2226b927d481f6c2`  
		Last Modified: Fri, 12 Jan 2024 00:22:27 GMT  
		Size: 1.4 MB (1378086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b40dea782b667ff8af1e03dac7c4a5706cec03d808f08850d4f3dcccfccae4`  
		Last Modified: Fri, 12 Jan 2024 00:22:35 GMT  
		Size: 203.2 MB (203160983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:fa5be89cdcd3f0c6819d61a6f3eb4e4b02ae57a2b83144c7c1f9fee7aff8b799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2207640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be979b4f291b821a81a7ba23a18ac3f272a80dc7e4df58519652b8f7f7b2d131`

```dockerfile
```

-	Layers:
	-	`sha256:a9f17534fd120369ad91084cce6d0d265afae8b0caaf84fbfe8bc5d02a29d2d2`  
		Last Modified: Fri, 12 Jan 2024 00:22:27 GMT  
		Size: 2.2 MB (2190181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f65d7a6275da4a24c699bf2f158f347c1c2258faf160f4d52e3ea7d0943ed806`  
		Last Modified: Fri, 12 Jan 2024 00:22:27 GMT  
		Size: 17.5 KB (17459 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1d40adc32a811c34de3a5ff584567d7680c03c5e7445400d7b960d22f5c65750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232486974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3ee5fadb4b9b1bf3c38f0d06e964a19e362f3ab4f176c929f5ebdf4f65b904`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Sat, 06 Jan 2024 01:52:17 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jan 2024 01:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jan 2024 01:52:17 GMT
ENV JAVA_VERSION=23-ea+4
# Sat, 06 Jan 2024 01:52:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='9a68dc2301a1ab9d674095ba14205b79ba23dd83002077ae6777edc820e789d3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='1a7293d34fcb6c1b9f5b0bfc74aabc4e695b0e6d6b6778172d59596b19db6e4e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jan 2024 01:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc02ea368438444f96ca14e22446135689f64999554dfd8cd20ab0b7c7a2913e`  
		Last Modified: Wed, 20 Dec 2023 10:24:06 GMT  
		Size: 1.4 MB (1361921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f827ee181ab9cd6382e33e196f727e8b1db325898cf3d29dbbbe82f30c8f5e31`  
		Last Modified: Tue, 09 Jan 2024 02:22:06 GMT  
		Size: 201.1 MB (201061001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:6d1c0f4968ec65b940ad4dbdc6e4bb53451ee917c04d1a74359f34416f5b600d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190075d72de3c0f3ef7d63c5586258d9045c7a5d14bc2926de8dcdac94ab524e`

```dockerfile
```

-	Layers:
	-	`sha256:ab9757c7b19bbfce9c6f871783e1f752a4ebe6d317cef7baa12bbff33e21003d`  
		Last Modified: Tue, 09 Jan 2024 02:22:01 GMT  
		Size: 2.2 MB (2189543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed15576265c7a6a69a6573035b19132251b36f0e090337d05a9b81db0a323afc`  
		Last Modified: Tue, 09 Jan 2024 02:22:01 GMT  
		Size: 17.3 KB (17306 bytes)  
		MIME: application/vnd.in-toto+json
