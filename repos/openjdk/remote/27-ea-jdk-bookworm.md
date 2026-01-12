## `openjdk:27-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:a50d912132a67045d4f2a8099648c4190b40a6938fa820962d1ff1885d92a895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:c6578367b40c74f82913bead74fca90b89288dbbbe185b2437a9887b85e766b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381884103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cbd75b95455eb94cce089fbc4d6063a0770b949ea2566e52519938ad81991e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:08:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:08:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 12 Jan 2026 20:08:41 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:08:41 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:08:41 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:08:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:08:41 GMT
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
	-	`sha256:eaa2c81a68000880225b59aa60533156b6dde05f8e5ae6f1bbd42a899719ebd1`  
		Last Modified: Mon, 12 Jan 2026 20:09:20 GMT  
		Size: 16.9 MB (16944907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fe15c97c7f399ddf25f70c0c3445fd07f4530484e79687fc43321b3ee1fc52`  
		Last Modified: Mon, 12 Jan 2026 20:12:49 GMT  
		Size: 228.0 MB (228032966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:5c80baf3cd55a29cdafaf1db1f32e6db2a7047f1402e1883627361ec5d810027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5248135669b52cb06db1830809a9bbd6265eb2459dd0159e11981289e7b671fe`

```dockerfile
```

-	Layers:
	-	`sha256:62436aea14a720cb22b832e2886e34081f3fc88d5c9742b38ec652ed07fb0e7a`  
		Last Modified: Mon, 12 Jan 2026 22:26:15 GMT  
		Size: 8.7 MB (8668228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94cbb01ad73e9ce54e062abce2bdf2be1bd63be47c09f9698874d15c3726e39a`  
		Last Modified: Mon, 12 Jan 2026 22:26:16 GMT  
		Size: 17.9 KB (17922 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f71eca4173525fbce81953f87473ad9e9e4b1681ee5f553da70b62970599be2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.0 MB (380011177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d92cdeb63a5dd5b701719734f9b3c15d07117f52abaf75cbc517ee23615892e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:09:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:09:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 12 Jan 2026 20:09:31 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:09:31 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:09:31 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:09:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:09:31 GMT
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
	-	`sha256:2f41402772fec1617da3d63d38c6ee8140ddfbf0eb595ad7b96c41a82f63898b`  
		Last Modified: Mon, 12 Jan 2026 20:10:22 GMT  
		Size: 17.7 MB (17728457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301cd2d31ab3188104f0506e2f8a30ea5484879b36bc855d6554866b07b8f30a`  
		Last Modified: Mon, 12 Jan 2026 20:10:22 GMT  
		Size: 226.0 MB (225954025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:bc4a3f83dd48d33569267106bca43564fbce04b7ecfcaa9c8e89bd3bf31c71d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94877a40e6faa954b915fc0d302c0ca39459fe28f68dd7aaf2fd634f58783e1d`

```dockerfile
```

-	Layers:
	-	`sha256:851fa2df9529e9d6894c1118573cc71cf777a63a33c0f4916c3a22aab72e4d49`  
		Last Modified: Mon, 12 Jan 2026 22:26:24 GMT  
		Size: 8.8 MB (8805073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0595a97c77ad1de599efe168086314aae418f3a9aca41fcca970ad7f44607db1`  
		Last Modified: Mon, 12 Jan 2026 22:26:25 GMT  
		Size: 18.0 KB (18041 bytes)  
		MIME: application/vnd.in-toto+json
