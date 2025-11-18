## `openjdk:26-ea-24-trixie`

```console
$ docker pull openjdk@sha256:fb33679fd5ccbe946ce64a75eb9bb0d8e7c9854aaf403ff7ce49b93156c86ad4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-24-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:7a5da3bb16c24715284cf02429bbc39a3ffe1c27bc3df3931d197be45d283332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 MB (386583324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c167d015ba44a72eb4ddba3fc88dca50239654f9ac7b2c65cc658c4389dca314`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 10:26:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:27:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 18 Nov 2025 10:27:02 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 10:27:02 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:27:02 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 10:27:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='4ba2cf8ca6a66fbea892ba55048f82d8cd4fabe95d9364ac28a79b282c6207f8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6f947b5c9fa605b41f4890ef6e09f2c0c321215681497f2174efa10adfab326'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 18 Nov 2025 10:27:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae668646f447b181fe300ae6756351b6167aa2578be449b167ba79ed4926798`  
		Last Modified: Tue, 18 Nov 2025 05:11:30 GMT  
		Size: 25.6 MB (25613858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2e6e687b6ce78177a4cac678dd533c8e72b97469f030783b6bb491f681fd4c`  
		Last Modified: Tue, 18 Nov 2025 06:39:26 GMT  
		Size: 67.8 MB (67779054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe0ca4ea4e03c17a859d37aa15297b38afed1c655a4c554f52ec9079fc8cf60`  
		Last Modified: Tue, 18 Nov 2025 10:27:37 GMT  
		Size: 16.1 MB (16061649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b77781734aa131bee404e3d01c0b563991e72ca40098291f35f9eb8c5018d15`  
		Last Modified: Tue, 18 Nov 2025 13:25:16 GMT  
		Size: 227.8 MB (227839216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-24-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:e89dfbfdbc865e27b8c9c834f5b71cf3f3030a93f182d88c1262648ac11224c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8527856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76bfd2beeccca909860b6a7af8b56065895509bfbad8d00476e24578b0d8363`

```dockerfile
```

-	Layers:
	-	`sha256:49a908f6086c13380fe695674622b35c57d5484f4e17b7314e74bca3eb69cbc1`  
		Last Modified: Tue, 18 Nov 2025 13:23:34 GMT  
		Size: 8.5 MB (8509943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee15207fb2fc8e4e461fad894f37b11ce7c533a01c4af70049ba65309f6a646`  
		Last Modified: Tue, 18 Nov 2025 13:23:35 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-24-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:002658181030174c0b74efa2bfc50f6f29cf3b11d72dc177789fe354f851050d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 MB (384015283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d77df595ad28677154c3efb61ebc46f64be7cf2e82d3d0f1cf591bd03983f31`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:43:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:43:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 18 Nov 2025 06:43:12 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:43:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:43:12 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 06:43:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='4ba2cf8ca6a66fbea892ba55048f82d8cd4fabe95d9364ac28a79b282c6207f8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6f947b5c9fa605b41f4890ef6e09f2c0c321215681497f2174efa10adfab326'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 18 Nov 2025 06:43:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14656e63ca309d8cfd09d01a9dbb3d1ea2d59a5efe7d40b9716f822e821385ab`  
		Last Modified: Tue, 18 Nov 2025 03:27:58 GMT  
		Size: 25.0 MB (25021011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9898fed0b4a62008cd3a65adf14beaff9f7a6dbe46176b901f31b3a21db4c6ab`  
		Last Modified: Tue, 18 Nov 2025 05:39:53 GMT  
		Size: 67.6 MB (67584762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a65cbde52b7a9f6f7d2f56f40b187864703af947ffc00445be4ec354d186c6`  
		Last Modified: Tue, 18 Nov 2025 06:43:48 GMT  
		Size: 16.1 MB (16070645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8db234f6cdac2b3582ab0f7e66ae39a47fa60d012299ec5ec570227f651a23e`  
		Last Modified: Tue, 18 Nov 2025 08:15:44 GMT  
		Size: 225.7 MB (225688633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-24-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:008c68daf64ff0a29b449c67f81108344b534e823cc23ec3b7549fd8fccabd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8722765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca70d527f82d15df94111989764ab2e5b82a508ad2765ac5cde301bb1f9db02c`

```dockerfile
```

-	Layers:
	-	`sha256:0203e421b96a34793794f51a3a49d358996d704fbfe4abcdb0bf12f68bca2135`  
		Last Modified: Tue, 18 Nov 2025 07:25:20 GMT  
		Size: 8.7 MB (8704733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa66357dcda0d5ff0778a572dbc278f73df5eec4557ddb72ff3dd75b4f35d6c0`  
		Last Modified: Tue, 18 Nov 2025 07:25:21 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
