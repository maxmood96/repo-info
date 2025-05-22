## `openjdk:25-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:6504ca8099f45700ba25bd71c24570c396b7a3ec0407915ad876b2cc1af44607
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:6f76448ede8b0fc14c0b6889ca51319fbe385e82647af56f1b0f40e68d00333e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245831733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7317f56afb5f0a945cb52bfeeea0edb26696abe989f1cf28444c8fdf72e4fbdb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 May 2025 00:48:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 16 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f2d8788017e8ffb7bf559492efe8fb46d20d613df50a5eafaed7a8344a54a5bb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f1c62c8b60be587c98a541129878b43e854c0fe167710878aa719e7f3dbefa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eac6016fdfb36636f25ff3c94e2e0a83d33c640d269151452fe83500c72e52d`  
		Last Modified: Wed, 21 May 2025 23:24:15 GMT  
		Size: 4.0 MB (4019994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9cb71c0cbf7f4409a519bed61605f77b9be278c250646b5ad31787c5455de7`  
		Last Modified: Wed, 21 May 2025 23:24:18 GMT  
		Size: 213.6 MB (213586409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:30675de57d48c1dfdf2d17880d609c0e5b3a05902c43d3266591f2f46d9702ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9e44a79b72062d1b75a3c6184a9ef98c883baf3dd656a095ebfd875cbed922`

```dockerfile
```

-	Layers:
	-	`sha256:a8adc5f86df10321104ee39d38166bfdafc6e49426baf25ee07ddae6eb70699a`  
		Last Modified: Wed, 21 May 2025 23:24:15 GMT  
		Size: 2.6 MB (2552703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30a85a5719d49111ba17da04d2478dc88e7f3073969841b8b708761648c9d66`  
		Last Modified: Wed, 21 May 2025 23:24:15 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f3490d97d608b595186943e35b75fa503b11ddd531cd81eb7e5f5b4b79a31709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243274966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6dc73dc27524f6a4298191b7b5992dbb2a54b1cee7d0a2329f166d096d27f1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 16 May 2025 00:48:12 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 May 2025 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 16 May 2025 00:48:12 GMT
ENV JAVA_VERSION=25-ea+23
# Fri, 16 May 2025 00:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f2d8788017e8ffb7bf559492efe8fb46d20d613df50a5eafaed7a8344a54a5bb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/23/GPL/openjdk-25-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f1c62c8b60be587c98a541129878b43e854c0fe167710878aa719e7f3dbefa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 May 2025 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba55b79ef31d50f4f2617c67f15fd3189b2a1f953d7736811f97eb36b381d3a2`  
		Last Modified: Tue, 29 Apr 2025 20:30:21 GMT  
		Size: 3.8 MB (3833814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495c65caf8147348c10a0afbf3d0e04e45de9c99923205daeb3f07914e08e258`  
		Last Modified: Fri, 16 May 2025 20:56:05 GMT  
		Size: 211.4 MB (211374530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e0a58d433f97ed5d742cdd1c1874197adee60e8b5adc4c0eb691438a82f82529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2571962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde88039adb2e8a66414f0d034d1cbd079f542d746ac4dcc9a953ce1e6f0e96b`

```dockerfile
```

-	Layers:
	-	`sha256:942743efa26ace2baa9752c5f48b15fa5bb305e454374d49583e959488299199`  
		Last Modified: Fri, 16 May 2025 20:56:00 GMT  
		Size: 2.6 MB (2552305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1365ed8950992227a655f49a4261fa0457a69b186719db578708d0fc78eb42cf`  
		Last Modified: Fri, 16 May 2025 20:56:00 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
