## `openjdk:27-ea-slim-trixie`

```console
$ docker pull openjdk@sha256:0eae92b8e3fd0f81fa2313f198581831ecb5b899aa94fd576c9c94cfb2435b14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:9cb24de87af2856c29f588f08a8a69b6ea9129c8aed2183e61e820cc43e9ed18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260230009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baffd2d933779e75fb613748dec708eb72d57755a0793b42f6d6826c17534944`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 12 Jan 2026 20:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:08:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 12 Jan 2026 20:08:40 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:08:40 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:08:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:08:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4387d261aa047840fcbf450652b1e4ea58f76534a1c7fdd52fb754b8e344bfc5`  
		Last Modified: Mon, 12 Jan 2026 20:09:09 GMT  
		Size: 2.4 MB (2371045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a274bffb86fc5b6147c2c2a5d3769a43152128581173e9c79796a3e3adc5e5`  
		Last Modified: Mon, 12 Jan 2026 20:09:26 GMT  
		Size: 228.1 MB (228082431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:af438c1464a1a7b2fd933e26074b8c4a44af2358c4a3478508d38b559b6b7656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e244a949076c778f9e7179ca9db1d4fa214c4d54fc5b4aa670ed0b70c592d57`

```dockerfile
```

-	Layers:
	-	`sha256:33ddc477d305fa3018d565a7b4ea7eb88c9d1bbb4790e81bd5eaa72ad32d020a`  
		Last Modified: Mon, 12 Jan 2026 22:26:49 GMT  
		Size: 2.3 MB (2278777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92d7ca22d60a26f31121a2541f79a254379e3a5e839b23eb01bcfbcb4af19940`  
		Last Modified: Mon, 12 Jan 2026 22:26:50 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:139152c5a9841762871d8fdc3cd4a9612dd006577c9f3273286a25f2602b7b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258458841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7239cc41b5ab6b4e899da2b77795ab0b79898b9cc167021beb47dd47d6d107b4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 12 Jan 2026 20:08:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:09:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 12 Jan 2026 20:09:23 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:09:23 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 20:09:23 GMT
ENV JAVA_VERSION=27-ea+4
# Mon, 12 Jan 2026 20:09:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='382725d08eba5640408ba0143ed6e11ab9662d1e51349001ac3d08798c8d6e6c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/4/GPL/openjdk-27-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='22d88b67c9736507c6d435f7bda9282628ba0e1acf77519f30752dfb30f2f03c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 12 Jan 2026 20:09:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2139e9bc3c188c80bdfa24fd207be28056b7591868d025adc113b88a53c57f9c`  
		Last Modified: Mon, 12 Jan 2026 20:09:07 GMT  
		Size: 2.3 MB (2314136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1a6d636b4a47b2cdf33a05a71412a9e00d2a2c8e85d9a288fe52b383865376`  
		Last Modified: Mon, 12 Jan 2026 20:10:04 GMT  
		Size: 226.0 MB (226006069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:a0761fe68ff6447c4a902cd1c85fa66677e0624fe4965d38f088b6ab75125b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70a08bfbcc754e1d6976080f96cf855bfc9d1484f5606500016290c3bd77085`

```dockerfile
```

-	Layers:
	-	`sha256:ecd14a1e61bd033e895796af76892dbec5484989cfb0a3d0ed631f2b165ab684`  
		Last Modified: Mon, 12 Jan 2026 22:26:54 GMT  
		Size: 2.3 MB (2278463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ac501881eaa62dc9ae7ba3da3ea0d855eae94cb239a171b7f9c002b2013bb4`  
		Last Modified: Mon, 12 Jan 2026 22:26:55 GMT  
		Size: 18.3 KB (18254 bytes)  
		MIME: application/vnd.in-toto+json
