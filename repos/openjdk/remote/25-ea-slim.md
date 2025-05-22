## `openjdk:25-ea-slim`

```console
$ docker pull openjdk@sha256:34c01c78da46f84e9d55cdd00001afe46fd283e0edcd8818d97c4cfd31c34394
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-slim` - linux; amd64

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

### `openjdk:25-ea-slim` - unknown; unknown

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

### `openjdk:25-ea-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8eb6608cbf79634084debd3355066af1053d58eca15e2df4d0a6efac6ea6b180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243274862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce43dadc831b1b13c749d1c355b28b1e3f01c770a2dcf5354d71c16b9c964ebc`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 May 2025 00:48:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534846ac900e03a1a9681c93961912f7790334b9daba4996c1c1fb5a858bff00`  
		Last Modified: Thu, 22 May 2025 03:34:20 GMT  
		Size: 3.8 MB (3835231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ad8a9eebfb1f9247ea90a47df71bcf73bd36d29b4a784bdba77f0127d0c6d0`  
		Last Modified: Thu, 22 May 2025 03:34:26 GMT  
		Size: 211.4 MB (211374351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:72941d6f30cf87673d105f4238fe65d229786432fd095534314565c4022c3d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2572090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fe96a25bd817f7d9c0c28b72dee62c2f9b25e01ab2bc4d25eea4e1dfec381f`

```dockerfile
```

-	Layers:
	-	`sha256:eed5d72e08a2ff236753b5cb598cc21d7d2b2309c4e7ef5880b60d0382e68249`  
		Last Modified: Thu, 22 May 2025 03:34:20 GMT  
		Size: 2.6 MB (2552433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e75216e2298f763a764cc2c2d43fe366889252b7344f5a7cb16d9e9ec599acc`  
		Last Modified: Thu, 22 May 2025 03:34:20 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
