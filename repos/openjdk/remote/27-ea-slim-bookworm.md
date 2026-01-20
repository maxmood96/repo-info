## `openjdk:27-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:289df3ebb73d2216ff572c3da40da2bb78d66ec715bb48f0b8f7bcdb4e65d07f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:20f87483dd06dd0bff3e7f04a0e178245593e8048d4301c6bc292823afc03196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260341852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7f896d654384ae4a10edae4a2f244296f1849ba7d4bf3b7511fe1d9daa5d05`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:44:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:44:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 13 Jan 2026 02:44:33 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:44:33 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:44:33 GMT
ENV JAVA_VERSION=27-ea+4
# Tue, 13 Jan 2026 02:44:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 13 Jan 2026 02:44:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba12b512c489c9fd0722ab66f17c9182f28e88a489fd2ce76b095fbf171b2a79`  
		Last Modified: Tue, 13 Jan 2026 02:45:05 GMT  
		Size: 4.0 MB (4028233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e69684db133e253e657e3ee6372292a1a187c2f5faf40b5c2fd4f71fad276b`  
		Last Modified: Tue, 13 Jan 2026 02:44:59 GMT  
		Size: 228.1 MB (228085047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:d6ddce2582db9c2ee0cd378f29ddb16e4b47f35102635858ba05d11d839292f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6e02d602ad4ae0da659302fa6d201903dfb23b7012a1a3241046b40cee249`

```dockerfile
```

-	Layers:
	-	`sha256:3fdfeec1abe2930dc8c779590c9f9c324c8d090da77c8921b5e946cb916cab75`  
		Last Modified: Tue, 13 Jan 2026 04:25:16 GMT  
		Size: 2.6 MB (2649791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55615c115e9d9e715811e9a7fb782188cc7d78923d1b2d4079760108c3b40ab2`  
		Last Modified: Tue, 13 Jan 2026 04:25:17 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:58fdefdf5a6f06563225cfe6719c8adef8daa02886b4fd7122d9eb329f76958c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (257963949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c7a017813050ece3a96202b0ba3ec416fec98f940cf326ccf4e35d503b029a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:49:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 13 Jan 2026 02:49:12 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:49:12 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:49:12 GMT
ENV JAVA_VERSION=27-ea+4
# Tue, 13 Jan 2026 02:49:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 13 Jan 2026 02:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195baeda9de14daabfddd3e30e9c1000120bd1287225b0791fe12ec7668718d3`  
		Last Modified: Tue, 13 Jan 2026 02:49:43 GMT  
		Size: 3.9 MB (3851999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55e7bff96a928bf1bc19a6db49fb04c9f4533244891f375ad9a2e9742840456`  
		Last Modified: Tue, 13 Jan 2026 02:50:18 GMT  
		Size: 226.0 MB (226004061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:8010522f55a6c23ad7e1903921691206079fac584644839eec0181999b361f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4930d6858db58ffc43780289407fbc2d999daa97d0e97d1fd1f20b25d87373c4`

```dockerfile
```

-	Layers:
	-	`sha256:554ce229800bd1c5f87510e31b8ddb9d2bb6d493e7cb8799c5e6e82196775f84`  
		Last Modified: Tue, 13 Jan 2026 04:25:21 GMT  
		Size: 2.6 MB (2649425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1daf38b04e14003e11c67a795f96296adc7e2b535b8b527b85694d08c8968110`  
		Last Modified: Tue, 13 Jan 2026 02:49:32 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
