## `openjdk:25-ea-bookworm`

```console
$ docker pull openjdk@sha256:36e88686636e2856fd18f5fe3dc54f2bc3c5bf19452f97089e7328bb1bfc014d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:a92cb96db55a19f7bcd0906f38397d38fa53df319b358f6555dd3c30d5e326d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366794707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433361b1b4da32798ab549988a7728c34f57cfb8ac2521b39e75c6622ab90b6f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 10 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+22
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ce6d616a09c8fb4391dbe165428d33b1751a228581faf829ac0610db8120ddbf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='76b4d96328978d3ba01a6970ff47dd1f368e42e94a8ba51fb3260e07230de663'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c90882185fdca33ca361e61bd5fa4673fde35772f614dfde7b0db15d4ccb141`  
		Last Modified: Thu, 15 May 2025 20:35:28 GMT  
		Size: 16.9 MB (16943484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98164f10dfcb4a07c43da76fae4b4e551fc011b7525fa19515138e56606851a0`  
		Last Modified: Thu, 15 May 2025 20:35:38 GMT  
		Size: 213.0 MB (212954416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:fb42888daa945eab297fa302fa118c68a2d3d584239678fbdae0c61beb25e9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8451953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e233d8ba7cca5a7503516fb4146fcd86fb7fa1e871ef27686a401c1ba9a4bfe7`

```dockerfile
```

-	Layers:
	-	`sha256:a3aabe4ea81148e4395f928114d5cbcd05d828bd7ab299d721d8b8ef1c23f1b2`  
		Last Modified: Mon, 12 May 2025 19:12:52 GMT  
		Size: 8.4 MB (8433335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05773fe0bfb21ed17919ae8e031e535f3369861a6f9ddb0413e265a7e0d3d6f2`  
		Last Modified: Mon, 12 May 2025 19:12:52 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a2e91a9e2668e360b5db6fe2f39d58eadd7ed4d1a1307ccd022ba9e4be639cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364723612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e1f2447082cdf5f47402427a9005f4646b6b3792ff0a5e0916ae87f1be0e8d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 10 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 10 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+22
# Sat, 10 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='ce6d616a09c8fb4391dbe165428d33b1751a228581faf829ac0610db8120ddbf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='76b4d96328978d3ba01a6970ff47dd1f368e42e94a8ba51fb3260e07230de663'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Thu, 08 May 2025 17:04:49 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6522f2c436113f78d937550968212260622e37a75b542b1462c1565f2e591e1`  
		Last Modified: Fri, 09 May 2025 10:41:56 GMT  
		Size: 17.7 MB (17727592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263e19c351c5758bcf1ed30c84d4367c864c94d1f6acb1049ca57cf6b09374f1`  
		Last Modified: Thu, 15 May 2025 20:10:53 GMT  
		Size: 210.8 MB (210768431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:bd2426bda192ed61b1f80bb2bd85391e7d16a5e82fa0359701fc020c3f2a590a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8588964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0276d1d8edcad9f57b72014dfbead9e9efab9fbeb67b278f2415ba932955a5ca`

```dockerfile
```

-	Layers:
	-	`sha256:f7a85654276c5c8433f06c45a8de10de1ef6796e8ea63a5fa3e337dd1ca7263c`  
		Last Modified: Mon, 12 May 2025 19:22:46 GMT  
		Size: 8.6 MB (8570203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b144b1f7ab981e3f61a7d3bd9b9bba114d5f3e82add634fa1e5b51970640bbc`  
		Last Modified: Mon, 12 May 2025 19:22:45 GMT  
		Size: 18.8 KB (18761 bytes)  
		MIME: application/vnd.in-toto+json
