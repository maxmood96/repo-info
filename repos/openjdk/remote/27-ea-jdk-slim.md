## `openjdk:27-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:a18737e30bcaf3cb259fa5c2ca4655b71f09c0fd1a71b125e8d3c8066c321fe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:4ebb8d7be5bfb2970e5afe60654a77b1795146b4071d29e894e2541d38b2357f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260248046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c89dab8d7f6c8564127a495cea21f4b9ea221e273dfa89f5fa385e5c8fdc806`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:13:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:13:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 30 Dec 2025 00:13:20 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:13:20 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:13:20 GMT
ENV JAVA_VERSION=27-ea+3
# Tue, 30 Dec 2025 00:13:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 00:13:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c887b41485e670c9120cda4d6d7b8c4536d1a86acc642138ee3b43b5d6caf4f1`  
		Last Modified: Tue, 30 Dec 2025 00:13:51 GMT  
		Size: 2.4 MB (2370982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f129658ebf30a55fed622f394b5934e44d6d6dc5ba464e7d56ac792461d856c1`  
		Last Modified: Tue, 30 Dec 2025 00:14:03 GMT  
		Size: 228.1 MB (228100531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:7aef1a1f2f856c8567d4c8f057cdcaf8c58262549f1b0d0ce0a527b5dbedaaf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8025c5946b3c68f878c98a749b595ac536be68c2180166c2a924133333787136`

```dockerfile
```

-	Layers:
	-	`sha256:90a8e05f5268b78881eda62daefbcc204a5ceb70eb2c0c15a00814f5fcc8d35c`  
		Last Modified: Tue, 30 Dec 2025 04:25:24 GMT  
		Size: 2.3 MB (2278777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf85c7091f34feea9e6551457eab23f2457cc5cac8eb11a483c6bcf89d8dfa8`  
		Last Modified: Tue, 30 Dec 2025 04:25:25 GMT  
		Size: 18.1 KB (18087 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:583bbe50318e13e8b3556a329a646134ec30abc2775ca57223876998348d0e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258473510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdb6c87711dcfe53c164d5dcc2636f509c4e2d8d21bdd14263c233e615a3c33`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:12:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:13:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 30 Dec 2025 00:13:52 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:13:52 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:13:52 GMT
ENV JAVA_VERSION=27-ea+3
# Tue, 30 Dec 2025 00:13:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 30 Dec 2025 00:13:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aabdee59c6729da2d6bd2e193e295267ed4c51c853e096082c7b274b404b2d0`  
		Last Modified: Tue, 30 Dec 2025 00:13:02 GMT  
		Size: 2.3 MB (2314071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5b0818c4ece3641684178886ba3cac4c92e7117cd8f8c0e8fa0d479c8b2f06`  
		Last Modified: Tue, 30 Dec 2025 00:15:02 GMT  
		Size: 226.0 MB (226020803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:65e3eebc727a6d0d01711be8447726429c107c57f9f27fdf347ae59e05e14515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3c4a132000932aa705bb3550c9ee86df6ba0cf644750656b5929343ad2c29a`

```dockerfile
```

-	Layers:
	-	`sha256:7e542a5c573084b0391a793679faeab715db8a0ec6271dadb053e37612bd0a87`  
		Last Modified: Tue, 30 Dec 2025 04:25:28 GMT  
		Size: 2.3 MB (2278463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39f11a3759c5edfc039c2a28bf6d5aadf11321bba1f39e3c0deeb6304ede25f2`  
		Last Modified: Tue, 30 Dec 2025 04:25:29 GMT  
		Size: 18.3 KB (18255 bytes)  
		MIME: application/vnd.in-toto+json
