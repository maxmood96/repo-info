## `openjdk:28-ea-2-trixie`

```console
$ docker pull openjdk@sha256:e3a8930dbdc2fa6272f19d656643686338aa7b277ae9c414498dfa345608069c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-2-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:69c2f8e01cb8878c533dd72f436051471f6daa8b8f4575aaae1cbd3b0b8a0e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 MB (386300350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37865f749a986816be8d4ead7450049ef04c402fb80d02f66a7a679631fe6f8b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 16 Jun 2026 23:32:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:32:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Tue, 16 Jun 2026 23:32:26 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:26 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:26 GMT
ENV JAVA_VERSION=28-ea+2
# Tue, 16 Jun 2026 23:32:26 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='f76b8c907a5e747c088e4215cb0d0b5ddd0bfb0080b1c8dd6108628040ace495'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='47eb3a6535a8d4a9468ea18463225459e824139064bc48c6527e4574cdaa08ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b365b6ff7b7e310e1b9a88f996e65b89969c7fa450492b68249d1d1c38e0676`  
		Last Modified: Thu, 11 Jun 2026 00:42:51 GMT  
		Size: 25.6 MB (25635173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca884014342f240be01d391b498c3ec61b2f4af2c205e7e9a0b5ac2cb2f24c4`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 67.8 MB (67784745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb453500b0cbe8059247603fcd1b2f64fb8d14b85feb5603dd625c46e257d68`  
		Last Modified: Tue, 16 Jun 2026 23:32:51 GMT  
		Size: 16.1 MB (16065744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878a228bfe272edf636da79ce5329f226f8bb6f1771b9f2a5642cff9109a4d8e`  
		Last Modified: Tue, 16 Jun 2026 23:32:56 GMT  
		Size: 227.5 MB (227497567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-2-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:da7ae9d8c19a4cfe88fdf72d22919cf13fa0912f0d6495641b55806eadaac127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8526781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd84e60c59a03c2c9e19f79865b65593358bc3873b961d0486bb399039ac546f`

```dockerfile
```

-	Layers:
	-	`sha256:8461fdae75ed1fd6c4f143e6cba04f48e48afefbb8ec51898a4009b11b5b07c7`  
		Last Modified: Tue, 16 Jun 2026 23:32:51 GMT  
		Size: 8.5 MB (8508885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9f1ad0744852eca278fb2f97c514cdf4365298d9a2260b62062ae9a78d7f25b`  
		Last Modified: Tue, 16 Jun 2026 23:32:50 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-2-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ec09c972780f1bca5858e2acb78f3fccc34f7197f3c071a256cecfa6d9054ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.9 MB (383909475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa2800842c9658c4eecbfa9a59c50fe9f0387d74bfec8db978d16326cb798a4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 16 Jun 2026 23:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:32:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-28
# Tue, 16 Jun 2026 23:32:13 GMT
ENV PATH=/usr/local/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:13 GMT
ENV JAVA_VERSION=28-ea+2
# Tue, 16 Jun 2026 23:32:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='f76b8c907a5e747c088e4215cb0d0b5ddd0bfb0080b1c8dd6108628040ace495'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/2/GPL/openjdk-28-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='47eb3a6535a8d4a9468ea18463225459e824139064bc48c6527e4574cdaa08ae'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2ab02859108b91c1c26f2badd015b5215eb066b7ef4f3a22bd1536a8debe96`  
		Last Modified: Thu, 11 Jun 2026 00:44:32 GMT  
		Size: 25.0 MB (25026911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2e427d8856f71d8d3667d1c4d9274b8aca2bd9d228387c51c211909e51263f`  
		Last Modified: Thu, 11 Jun 2026 02:22:21 GMT  
		Size: 67.6 MB (67599934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bfeec79cde8123bd0694df2edcbfeebc33f9833cebc559fc151877ba1ccbb5`  
		Last Modified: Tue, 16 Jun 2026 23:32:38 GMT  
		Size: 16.1 MB (16071400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fe7c47ba500127da422c896a5ee6769bbfba1e1e12bbeae149bf0d45000b02`  
		Last Modified: Tue, 16 Jun 2026 23:32:43 GMT  
		Size: 225.5 MB (225533061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-2-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:c07e99f14d5c81f7a1694220b42f90e22ef273639ff7e02e5ca4c261ae6deeea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8721052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5106f978aac8542b7fcedbe3d28cf1e5e5a29b5fcd9903a542652f57ad0bc6`

```dockerfile
```

-	Layers:
	-	`sha256:0155933617e67b7faf694e193bb12045b0043e3a78b3484ccffcafb65ac2df13`  
		Last Modified: Tue, 16 Jun 2026 23:32:38 GMT  
		Size: 8.7 MB (8703038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba4e94ecb5902a0804b33dd136d8820e08497af061e90b705800763626ac0776`  
		Last Modified: Tue, 16 Jun 2026 23:32:37 GMT  
		Size: 18.0 KB (18014 bytes)  
		MIME: application/vnd.in-toto+json
