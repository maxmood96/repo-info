## `openjdk:27-ea-11-slim`

```console
$ docker pull openjdk@sha256:1526e7ce04ef18d1d133a34937d2c128fa5bdf45803a12d5cdffa07a8d0e0f59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-11-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:8320ea71905c59087e8b3edff20bbd7f2d3e85bd2b272ff8628a1057889c5cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260737833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ecab2eaa7af5c26023b5f3504b30ce33e812fbc46828c9183017322ae1277`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 21:25:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 21:25:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 02 Mar 2026 21:25:23 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 21:25:23 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 21:25:23 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:25:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='75a300b52539589c8c4b172ef292d5b58486de4d88d774be659975bc661767bf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='3bf27bc49545e677311a0eab8a838953f4726191499accef492c7feaf801e429'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Mar 2026 21:25:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc960fd093ee6775f3e987d7e8e59abd32810a2ad0b137528464508fb881edec`  
		Last Modified: Mon, 02 Mar 2026 21:25:42 GMT  
		Size: 2.4 MB (2370992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2f63534b73e243ef0099ce50c63942df04f2dd53c838a1117eb58bb84dbe31`  
		Last Modified: Mon, 02 Mar 2026 21:25:47 GMT  
		Size: 228.6 MB (228588209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-11-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:d06e866af71528d10b927a7d2620cb47245c2054cad5a9a5f06ea7e4cb11c4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146a18c4366edf0616006bda50bc68b079a8a983e8e31d00941e847ca620a965`

```dockerfile
```

-	Layers:
	-	`sha256:00471e6095c51b6b81590c8ffda81f34f8922b2d6344328963dd665f48d32b6d`  
		Last Modified: Mon, 02 Mar 2026 21:25:42 GMT  
		Size: 2.3 MB (2278857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d7fb497102408adfede167322c0da9ee2cbb621969781293a1f9e1b987cc593`  
		Last Modified: Mon, 02 Mar 2026 21:25:42 GMT  
		Size: 18.1 KB (18108 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-11-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f9d1c9457f81944e99fa7c9ef85a836923e37533e0eee52de1f6c1726e191a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258986853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ad848f2edebfff6eb8ca96f77d0c2f66b105ab38e231cc12bb4c2a963b0cd5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 21:24:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Mar 2026 21:24:51 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 02 Mar 2026 21:24:51 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 21:24:51 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 21:24:51 GMT
ENV JAVA_VERSION=27-ea+11
# Mon, 02 Mar 2026 21:24:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='75a300b52539589c8c4b172ef292d5b58486de4d88d774be659975bc661767bf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/11/GPL/openjdk-27-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='3bf27bc49545e677311a0eab8a838953f4726191499accef492c7feaf801e429'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Mar 2026 21:24:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d9a50fc775acfd02805831cc381851ddf7c66875388affa1f16ef77c66ad9b`  
		Last Modified: Mon, 02 Mar 2026 21:25:12 GMT  
		Size: 2.3 MB (2314378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e985cea453cf1668deb77d1c9e4d822161ad7cc2e2094306d5519905b95d39`  
		Last Modified: Mon, 02 Mar 2026 21:25:16 GMT  
		Size: 226.5 MB (226532377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-11-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:408aba96cee3c380b402062bd861e1ebc092748049ba0855a381343ce8aa8a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295ba853d388f4b053e2e23a5b59f77a1429f17a985a03eeee84db64cb34d5f6`

```dockerfile
```

-	Layers:
	-	`sha256:1a14b7e4e52ae7a439779d4358682e82771b7e55d80a4bc3fef3b1ce730e8e19`  
		Last Modified: Mon, 02 Mar 2026 21:25:12 GMT  
		Size: 2.3 MB (2278543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8a54bb4618aca27ad1a2f85b6da6ad6fec67d4f5007d3b9a1e4f83c9e5aa0c`  
		Last Modified: Mon, 02 Mar 2026 21:25:12 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
