## `openjdk:23-jdk-slim`

```console
$ docker pull openjdk@sha256:665e68650bbe98e25b91c251139d3337e8153247b996dbca956eaa897c8c4c43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:8d37531e47603faba32327e6ac103c3607524d4406df79334a6f689d41aa0835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243616289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0f8fb2dd356ed2f7e24a976cc0ac902bda128738811dbb28c8ec38aeaa8686`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Fri, 24 May 2024 06:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 May 2024 06:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 24 May 2024 06:48:12 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 May 2024 06:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 24 May 2024 06:48:12 GMT
ENV JAVA_VERSION=23-ea+24
# Fri, 24 May 2024 06:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eebed7702933983781b97d468d8772f419c150d1c7354f82f15dd07d79be2b17'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ff14d6b86a66b88540ffd39b93e2e1ce8a529048d0ffbd3a5ff5b5dd14f8345'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 24 May 2024 06:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c94aee69c7909e01a524dbd5b0dbfda48972ab79cd587e461eede366480a02`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 3.8 MB (3821762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25073d4e583ebc49a9f78d28b70141593ea666bf036f95b03d8fbd89e3a4a4f0`  
		Last Modified: Wed, 29 May 2024 23:01:28 GMT  
		Size: 210.6 MB (210644116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:41f91926caa57daf9376e0a50d7d01018e47f314ccd39cb021c8dcbf3bd1bbcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1522124f78f59fcff1c32a9e4dd8df284fd4f02b40c8af20f80f76ef6f276afa`

```dockerfile
```

-	Layers:
	-	`sha256:b863dcc3161bde71111bb9de4bf7f857555873271c73178f8595e84114561e23`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 2.3 MB (2346317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1215d2803a0710d7d01f5250bef69c60fe9b93768201f44125d89dbf32f70a0`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 19.2 KB (19181 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:408c1467949301835af51afd59fa185ab1ebdf2c67e4ae7db4291630cc949354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240604955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1756ff20f0ff2436b84107f97d98c1c7531a20138849356db59d92f5de0307e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Fri, 17 May 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 17 May 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 17 May 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 May 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 17 May 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+23
# Fri, 17 May 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/23/GPL/openjdk-23-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='ebb29aa3b7c39ccf29ce564c797c5723b7355880f5dafd239570f7e7f2166bfe'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/23/GPL/openjdk-23-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='feef29529ab1660b95345ebbc6f47ba2823e28e87596225a25d2c45fc4537f29'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 17 May 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8b1f64e0339e4f92e86a0e708211f334b1d646da5a099781f36253c76f5505`  
		Last Modified: Tue, 14 May 2024 18:13:15 GMT  
		Size: 3.6 MB (3629809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec4edf20c8f946e3ec626db59b4102f61105e95d43036cc35b1542ce527d888`  
		Last Modified: Fri, 17 May 2024 19:47:42 GMT  
		Size: 207.8 MB (207795643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:f84d651b83ba0bd99e6bd851466ceac737c66258b31a65f4806169ead0af095c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28609569c58dabc0cda199ae77d13eac4b2aec13e7308e2b856d95713a6c98de`

```dockerfile
```

-	Layers:
	-	`sha256:022d8a9e9442053576220ca8d9736890424b0631ef45b662d4d42182466a7fe0`  
		Last Modified: Fri, 17 May 2024 19:47:38 GMT  
		Size: 2.3 MB (2346546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce785af6a5fd9b734bdd446419ca4a6c012b70a19718b9a652ec239753a441b7`  
		Last Modified: Fri, 17 May 2024 19:47:37 GMT  
		Size: 19.2 KB (19207 bytes)  
		MIME: application/vnd.in-toto+json
