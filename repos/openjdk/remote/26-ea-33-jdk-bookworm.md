## `openjdk:26-ea-33-jdk-bookworm`

```console
$ docker pull openjdk@sha256:da0c8e629ac7fe4e6cdb6cb372086056d94267ed8b7f8709ebf414b1be4ed5b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-33-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:be96ce19e22191fff663dc20021bec1a3840b9d772376565e879a8c5ae8af3f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.8 MB (381844598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01bd7da79aa074a2c111c9e40994a041a1bb94b6b4c0e41cacf57e49d0ee4c3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 30 Jan 2026 23:40:23 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:23 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:23 GMT
ENV JAVA_VERSION=26-ea+33
# Fri, 30 Jan 2026 23:40:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6`  
		Last Modified: Tue, 13 Jan 2026 03:53:27 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a79ed52e4802446d7d6257171ea7485821a26c7a39365c52c77d6b9ee7d60d5`  
		Last Modified: Fri, 30 Jan 2026 23:40:49 GMT  
		Size: 16.9 MB (16944829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcee9f281ab9de0d858a48249e24ec6e9814bbd0dc1d124069dbe06d9b79e96`  
		Last Modified: Fri, 30 Jan 2026 23:40:53 GMT  
		Size: 228.0 MB (227985447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:263a367dce9f0fb34ff9b0a63994eb31b57c1d7f00bda243fa3f279ae6b614d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d825021035d15b84a722570e015937b1aa0c0bc97ec1e069495b9aad0fe493a`

```dockerfile
```

-	Layers:
	-	`sha256:012e31991df094fb5d01898c742d3912ef7559177aa7e70bae23f360a9fe3398`  
		Last Modified: Fri, 30 Jan 2026 23:40:49 GMT  
		Size: 8.7 MB (8668879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb4fa2a033fdd286ff43cf602989f9025d6cc9eb1dc1bdfe19d05f187e6a5b1`  
		Last Modified: Fri, 30 Jan 2026 23:40:48 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-33-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:93fa6ed3e75dbc4904052055d35e1ff0bdb502ab0e5eef95f20feb297f0dbde4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.1 MB (380075634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4540056a420f30f380b9f25749291ad94573ec21a35eb81d322d363643a0e8c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 30 Jan 2026 23:40:15 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:15 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:15 GMT
ENV JAVA_VERSION=26-ea+33
# Fri, 30 Jan 2026 23:40:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ad46596f06c934001fa6d7bea3d1508b0bb616cffb71004efd5bada56884f`  
		Last Modified: Tue, 13 Jan 2026 03:57:05 GMT  
		Size: 64.5 MB (64479462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb948ab6be17dab8d6d297cc0af44025868183c10da10b1f409fb706fc55ac4`  
		Last Modified: Fri, 30 Jan 2026 23:40:41 GMT  
		Size: 17.7 MB (17728502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bfb9aef07b48a1b2ac0ea92107033205a4ee7384c91bb9936a8611458c935b`  
		Last Modified: Fri, 30 Jan 2026 23:40:45 GMT  
		Size: 225.9 MB (225896784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4c99ed81d90ee816d2a65a690ca1eb30d418540f3abdd42b0a970a6a18cb91f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97afb90f6ad5164f2d908368529d9be77e439d867db7df78829b02bbad8216a7`

```dockerfile
```

-	Layers:
	-	`sha256:070dd8a69192f57c2dad3b97b2aed60f61b8d6b779c24161452c1e00f2a73e36`  
		Last Modified: Fri, 30 Jan 2026 23:40:40 GMT  
		Size: 8.8 MB (8805724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e00f59f67a88e567ce16da9b541e93c250a9b760ceb96d80eab6dd2efc8f20d6`  
		Last Modified: Fri, 30 Jan 2026 23:40:40 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
