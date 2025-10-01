## `openjdk:26-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:5be22161570041c14b93cbb54a7012832d6b20963125d097cc1b55d0f2beee48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:9457b93edbcf5489a19804a256d9a503d8abb7b0d358e3af42fb56a82acb73f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257910265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2946c92916f05d427ff6a46458aa95b31489752c73410508e32bf99b363f30a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Sep 2025 18:48:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 26 Sep 2025 18:48:12 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='0a80f3aa3279fbcd36b9247a873bc99b3688ce092a970c08ff3788e2fac99351'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='d12fc689cf8b2e7c1b503472b988320ad15693d9b40c3e877e9f78aae6fb82a1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7079b30cfe8b864d6780efc5bad1566466fb6bca0e8d9a677b3bc549d1eb4be9`  
		Last Modified: Tue, 30 Sep 2025 00:18:10 GMT  
		Size: 2.4 MB (2371122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946b995475af8f478f4bb1113d5ca05fb46f1356422dca3a9f83512d364df91e`  
		Last Modified: Tue, 30 Sep 2025 21:34:41 GMT  
		Size: 225.8 MB (225761377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:071f9a6482e80d8d3ff3e482bc6ccd2838f65e1634f8302a7ff8b9d2fa0b1976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1773ca070cb7f9e4ee5373c81604b7dca040f05c7c8f9c0db257dcdf00941e4`

```dockerfile
```

-	Layers:
	-	`sha256:d648f88a72668013102769cc66fdf4d066a8b02fa53a2eb8c34956a7fe4b1374`  
		Last Modified: Tue, 30 Sep 2025 21:32:38 GMT  
		Size: 2.3 MB (2282504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97b2df4707f7ee7be4e1024e495715bf819197f52d88d610d68f4ae50c4584f6`  
		Last Modified: Tue, 30 Sep 2025 21:32:39 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3e875ff086ae24368d31d8e46650883e69fc2978e4c18f2f86755e4f49eb37d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256109885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24191b0844c9947ac6c5ec39f5cba44e259cd611e92590e2cc36cd30bcddfe81`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Sep 2025 18:48:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 26 Sep 2025 18:48:12 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='0a80f3aa3279fbcd36b9247a873bc99b3688ce092a970c08ff3788e2fac99351'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='d12fc689cf8b2e7c1b503472b988320ad15693d9b40c3e877e9f78aae6fb82a1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531a7d82847bcb14231685b1228b2ea135fabe4dff05a00b4ccc2e325ad3fad4`  
		Last Modified: Tue, 30 Sep 2025 00:21:21 GMT  
		Size: 2.3 MB (2314258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659e03de74516d5e4c8b7dbfc418738af6cad0b692d5316746c418b993cee2eb`  
		Last Modified: Tue, 30 Sep 2025 13:23:53 GMT  
		Size: 223.7 MB (223654785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:236185a3a3313deacb9ff54a463687e1a6941c1866439c7a0a4af22e226327c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151ffa883fba39a354278e941434205016d3b20b3a4ade64e0b27313f5516cfc`

```dockerfile
```

-	Layers:
	-	`sha256:4a8c03bf7c38092c338ba6ed3a34f35193752dc6db345af1afefbfaf4c29d898`  
		Last Modified: Tue, 30 Sep 2025 12:23:35 GMT  
		Size: 2.3 MB (2282238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec01f44df90596c31c7f50a72b7ae623ea929eb6b377f3cd80a7eb38b9956cc`  
		Last Modified: Tue, 30 Sep 2025 12:23:35 GMT  
		Size: 19.6 KB (19627 bytes)  
		MIME: application/vnd.in-toto+json
