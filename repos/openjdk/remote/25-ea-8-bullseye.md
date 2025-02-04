## `openjdk:25-ea-8-bullseye`

```console
$ docker pull openjdk@sha256:6e02f44b545ad71a7d830fa28beac903c705f47cf03e009f2acf38eeb395e9bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-8-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:d9c27e656d3bda776ac9accfb8e8e3cdfa3df98f6ad1a6837dc29da4fe7125e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (349999242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e9bb1aad9a2302123306f433c616d058541ea45f84110f5846da40e55dee95`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 31 Jan 2025 01:53:00 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:53:00 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='1463f6f26464b27899d02c4bba0e2eb7f8b8dda88afb590c31c882a4ee3aeb68'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='fa9c00fcd40d033dce2058b91f5c8b689fc492bd1f0c6062729915d333b82ff1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 05:19:08 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295b0ba61754b886b60ea309e9b5bdd9ad296320f4e93f3eb600bdf36ee402a1`  
		Last Modified: Tue, 04 Feb 2025 06:14:24 GMT  
		Size: 14.1 MB (14071409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371ee210b1a9e3a527c5ad3fb3202916b9a6b2fc34c0078c1216f4f77bf15c65`  
		Last Modified: Tue, 04 Feb 2025 06:14:27 GMT  
		Size: 211.9 MB (211878772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-8-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:a0a9188d1344e2984e937a4797c5d962b9667281d093ed6a6454442b3fb04279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8382767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd04d334dc5f0bb48ff2d97bfcb0d7e7f06baa4f96c372edaff1b9b36c409a8`

```dockerfile
```

-	Layers:
	-	`sha256:e80d80a15359950b8213838db49897c96ef34b7c9dccc4df4f2e1eac03d6a4fe`  
		Last Modified: Tue, 04 Feb 2025 06:14:24 GMT  
		Size: 8.4 MB (8364166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:016308227c897b80305115dcea48a213e476f7290ea6b185ad7a19a6fd121247`  
		Last Modified: Tue, 04 Feb 2025 06:14:23 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a87e02d1b891381ed408c0cfaebfd1d2ec404e2ed73c222b2cae75dd8f75ce67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (348018094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9516310baa4f1f6f7b9cd03026c267236abd3d50b3d3f8e380898033ea51292f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 31 Jan 2025 01:53:00 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2025 01:53:00 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 01:53:00 GMT
ENV JAVA_VERSION=25-ea+8
# Fri, 31 Jan 2025 01:53:00 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='1463f6f26464b27899d02c4bba0e2eb7f8b8dda88afb590c31c882a4ee3aeb68'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/8/GPL/openjdk-25-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='fa9c00fcd40d033dce2058b91f5c8b689fc492bd1f0c6062729915d333b82ff1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 Jan 2025 01:53:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d131bb45427773e6afabd46e2adb4b244b25d4dabe87133f23082bb3234e33e0`  
		Last Modified: Wed, 22 Jan 2025 02:33:12 GMT  
		Size: 15.5 MB (15526310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f90eacda71530571359ffe8e9e31794dc7a5e65289fc70c27bab5630d3b6aa6`  
		Last Modified: Fri, 31 Jan 2025 22:30:09 GMT  
		Size: 209.8 MB (209849029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-8-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:aa34c28be1148eded9d442e3d8b0541de24914f34816a1c00e632042e7c2ebd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8483854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36ace64f0ba5d0bf5b687f20c6dcf115f4fccde86e401d9cb5d0080348fe49a`

```dockerfile
```

-	Layers:
	-	`sha256:cc560b77e451e8d88c04493e006c6520ba842548ca5d6508a52509e80d3c8254`  
		Last Modified: Fri, 31 Jan 2025 22:30:04 GMT  
		Size: 8.5 MB (8465110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab6b0b9c950fb69f723be007d72844cb07814e8e499003dc5f2a12ed71b4c73d`  
		Last Modified: Fri, 31 Jan 2025 22:30:03 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.in-toto+json
