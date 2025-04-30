## `openjdk:25-ea-20-jdk-bookworm`

```console
$ docker pull openjdk@sha256:030b8fd39972818799c58b5f412146bf818662226beab8286254ece5430572ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-20-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:e5ca998ac6f0bae603a86e04eab22c69ed7d326a158a67507b71ce33934d0ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.4 MB (366350009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2025b8c2a6b4582e162f6be968e3a02a7f104244d15da7fddd7ab4e981d8c297`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 25 Apr 2025 18:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='6bc1d37add3f10b8826fef26bfc5ab51183b308c32a12f08a18ee2b6d9e28111'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='e6b42d0f5816ea1fd6c27505ddf93dc11eae12fc2cc64b4139350d7c0acdd55a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352cba35a4f6158db21369882322a6130a6b1037d2049ff009c37c52f5110c88`  
		Last Modified: Mon, 28 Apr 2025 23:12:12 GMT  
		Size: 16.9 MB (16943420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866f4dcdf96d4e147b20084f0be6d3d459af37263789940007b0bca087d5ed6c`  
		Last Modified: Mon, 28 Apr 2025 23:12:15 GMT  
		Size: 212.5 MB (212509782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-20-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3153ac43192be6446caaf694e3ec4c73394a3949a0c2927ea3f01f1f8ace73dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8451953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a484e2b568e33e36e33129c87ecbf1d43e061d0c23de060d2f65e2edafc2bb`

```dockerfile
```

-	Layers:
	-	`sha256:6a8de957e4c06c991002a7a06fef22b00cbd9184ca61337ca6bc0a7f9d63c168`  
		Last Modified: Mon, 28 Apr 2025 23:12:12 GMT  
		Size: 8.4 MB (8433335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d91c6a194ccc87bbc310494bbeb58eb00f4b612d41806ac70bbda13f3b72794`  
		Last Modified: Mon, 28 Apr 2025 23:12:12 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-20-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:621da73da2127da3a3986cbc787cae426f9add0c34a24297779aa650f59a5171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.3 MB (364293747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1f4e61e8582372640d9a5f95b7df02d8e40c357ea76d699cf8e910d873ab1c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 25 Apr 2025 18:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='6bc1d37add3f10b8826fef26bfc5ab51183b308c32a12f08a18ee2b6d9e28111'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='e6b42d0f5816ea1fd6c27505ddf93dc11eae12fc2cc64b4139350d7c0acdd55a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Tue, 29 Apr 2025 18:37:11 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6522f2c436113f78d937550968212260622e37a75b542b1462c1565f2e591e1`  
		Last Modified: Wed, 30 Apr 2025 03:53:13 GMT  
		Size: 17.7 MB (17727592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430aa59aca4190f95d2c1fadb2a90bc177ffbcec7873bbb70c3837d8e5d15ab6`  
		Last Modified: Wed, 30 Apr 2025 03:53:17 GMT  
		Size: 210.3 MB (210338566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-20-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:bf62a26d4f11af1e170d190c97612f290f4d944cd0822ba56eed7b3620f8cc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8588964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60e826c02a7831ecd0b2be982908687dd557a0ebc17312264425296a0c6ddd0`

```dockerfile
```

-	Layers:
	-	`sha256:5f3bd2f0707e3b4ebde82f6817c7e3b0af1becd58f12302895f602c8fe008d10`  
		Last Modified: Wed, 30 Apr 2025 03:53:13 GMT  
		Size: 8.6 MB (8570203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bc86ea3c676276afca639f4db435184d51f6b52b9a9de117f4dd355bdd585c7`  
		Last Modified: Wed, 30 Apr 2025 03:53:12 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
