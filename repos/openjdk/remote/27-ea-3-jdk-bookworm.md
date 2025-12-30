## `openjdk:27-ea-3-jdk-bookworm`

```console
$ docker pull openjdk@sha256:b44411189a249d49a993bf7b2515e17a353f0db344abf70ff29470700371743f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-3-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:0c3af827e73805cfdae1d20e95410d18f5e2e50d702efbfa4562cb197e1f71ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381904675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a905517f7a6d19888db3ac3529919d0b693ccdb4cb44726281d6ee69380f03`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:45:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:45:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 30 Dec 2025 02:45:29 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:45:29 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 02:45:29 GMT
ENV JAVA_VERSION=27-ea+3
# Tue, 30 Dec 2025 02:45:29 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 02:45:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a858b7813255a9cb57d05f02b50978e5b5965b0cfc040288fa29905cdc65ad9a`  
		Last Modified: Tue, 30 Dec 2025 01:22:58 GMT  
		Size: 64.4 MB (64396090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69e816ce7029454fda55f242a825e88893696f1bc9fd3ba337dcaaffc4214d3`  
		Last Modified: Tue, 30 Dec 2025 02:46:07 GMT  
		Size: 16.9 MB (16944567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84a2c3484f5abb1e665f27d2de07918d8f055e05eed9a5278bf2a97c65e0f67`  
		Last Modified: Tue, 30 Dec 2025 02:46:40 GMT  
		Size: 228.1 MB (228053878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-3-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:9b89e8447c5fe096f1c273f964225bc51068e6f4b2b436d045405d3e2d1cf8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4ef709ca9d83b8b8af79a4188837119b64516173a2baf273209d7b236530ae`

```dockerfile
```

-	Layers:
	-	`sha256:edfce2a1951cd785ce35505d685b9d350d51e4d462df7ecf391493a2d9cfe528`  
		Last Modified: Tue, 30 Dec 2025 04:25:15 GMT  
		Size: 8.7 MB (8668228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83b48f51c22a3b498b10cf83a103bd3e8520f3c022a65c50f7e1e5c665144d5f`  
		Last Modified: Tue, 30 Dec 2025 04:25:16 GMT  
		Size: 17.9 KB (17920 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-3-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e5ead1b51cbbf5e3b0ea2219391b61350bc9007240ef35d20db09de875d73b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.0 MB (380021613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd393c520bd089ca553e805c0e1d36bca26a21a2e5b4ef7b958b92a36bf793`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:43:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:43:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 30 Dec 2025 02:43:42 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:43:42 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 02:43:42 GMT
ENV JAVA_VERSION=27-ea+3
# Tue, 30 Dec 2025 02:43:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 02:43:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885a684c982cb8679ba82c9c939ec2b3cfe9c823a68d404ebbc3ac75d14830df`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 64.4 MB (64371168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725435d8c18d40305937cd2d2c882ce4c3d07ade0e98a83092fc5ba3837218c9`  
		Last Modified: Tue, 30 Dec 2025 02:44:18 GMT  
		Size: 17.7 MB (17728400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be02c73b292d43cbb30a0fd4d2ce85d602644f729454a03f4e866176402a503`  
		Last Modified: Tue, 30 Dec 2025 02:44:27 GMT  
		Size: 226.0 MB (225964518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-3-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3f66ba664c5448b5f6c46471c28065527b6acabf1f5532d1c06b28137b677ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55abed0a5b868c44dc3f30c41f24a453f73e9c354684ce9781ffcd49572483f8`

```dockerfile
```

-	Layers:
	-	`sha256:5da0f8df1e1ff06b87c7b773b3ff7cdecef3e395f9114ba23ce55936837b13b3`  
		Last Modified: Tue, 30 Dec 2025 04:25:23 GMT  
		Size: 8.8 MB (8805073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a1dbda59e179cd2857d4891d3e7d1d90e1427e17e6d4a692c96d8966a789e46`  
		Last Modified: Tue, 30 Dec 2025 04:25:23 GMT  
		Size: 18.0 KB (18041 bytes)  
		MIME: application/vnd.in-toto+json
