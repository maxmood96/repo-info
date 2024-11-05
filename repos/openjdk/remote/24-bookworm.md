## `openjdk:24-bookworm`

```console
$ docker pull openjdk@sha256:179b06be15d766b452855bc3f283be9436aaa5e678186479ae8d0c6b09e8a5cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:81608764b85f172c3107d11fc56d9c0f71e07e1b76cb383f62606866479948e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.1 MB (367096902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b75dbc5e6cc97f7e182d1316a3fd5ff9c3611973eb9fd3aacd78ea5750d3e2e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 01 Nov 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+22
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='623a217a8f87e35d4ff793f172e2c66ac4abdd9ff21835d7ad8b1f0e1ad83fe4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9a0070483615cc2db61a47afaec955cc7be38ec88f75856307bee73c9f601cbd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b71aa9b770b5ff5d01ac3cee501ee1f2fa76e8bbe03e5059508d580576ed51`  
		Last Modified: Mon, 04 Nov 2024 23:07:37 GMT  
		Size: 16.9 MB (16943123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700ff5647eb47f26dbc163e9e0318ca839e5b96acf560ae8428356ef4410eb19`  
		Last Modified: Mon, 04 Nov 2024 23:07:40 GMT  
		Size: 212.2 MB (212157675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4857e17abd7adad3c44266ea4d65852e71257fe7dda53e695802158ece2b924a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8445653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ec506a2a85e57e440b17989368c34f79ccaa8737695f63212fc83bcef1a01c`

```dockerfile
```

-	Layers:
	-	`sha256:b4d79bc0f8b4288f527312a7a739dd81b95888ca30a7bee349e8714b2a6011d8`  
		Last Modified: Mon, 04 Nov 2024 23:07:37 GMT  
		Size: 8.4 MB (8427035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a7a55847f6a7de63876fb27c48b38fc52bb63ab5fd092112a83d3fcfedcfac`  
		Last Modified: Mon, 04 Nov 2024 23:07:37 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8da219d364589f7ecde12c3f23dbdd071100598689f939631d22bd9ed2587e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365682940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9068593bd21dc27b1ab7848df28ae172355a0f258459ad0120ac86682ab6809b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 25 Oct 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+21
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='c67029681a2f1c745c3a73366080881b2d349b4ffb9ce6a4e1e4b2c423555c5c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='3850e8de3f5cc9a22fabc0963a04d6205a9f242cf2cfc0d67a4399a54deb725e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f9c1d368f904fb8f826e7945c11c1d4c12bcf39b3a02ba58ac8421ea158c9d`  
		Last Modified: Fri, 25 Oct 2024 23:01:17 GMT  
		Size: 17.7 MB (17726979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfabafdf2ededeaabed03f84c52800c6d04d2636cb8facb0be6e048efe3f1919`  
		Last Modified: Fri, 25 Oct 2024 23:01:21 GMT  
		Size: 210.4 MB (210427105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:29685822197c3c425a10dbba244014bc3ecb7e04babbd0598a04d1f5c977c81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8582226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1922196c64122a55dff2cd36e272f9a83b8b3a7bfbfef2eeab67d2825e806d2`

```dockerfile
```

-	Layers:
	-	`sha256:e9c0c0fc65ff7d91510f317084f8360031bf752cc51ae1a859e33b6d9e2de60b`  
		Last Modified: Fri, 25 Oct 2024 23:01:16 GMT  
		Size: 8.6 MB (8563447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf379856e23bcd93bea2c3172d4ecc974c7895cc67bcefc79d79be8b62189c1a`  
		Last Modified: Fri, 25 Oct 2024 23:01:16 GMT  
		Size: 18.8 KB (18779 bytes)  
		MIME: application/vnd.in-toto+json
