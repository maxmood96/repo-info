## `openjdk:23-ea-8-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:e5a8097c44b0492ad13ce9932e9d80e9014d74ae75b2aee60b7ef55ea5938ad7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-8-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:53408b9cbaa8af0b5de6f17ff1f69cc636e825eef77e90320607a822462cee53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236307560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735f5001bf87416550eb9593c9d1c3cf1b5a83336a84077ae8e047bc34652ea8`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 02 Feb 2024 19:54:38 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 02 Feb 2024 19:54:38 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:54:38 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='3f36f003a7dbc52c00e66678dfd2c190be7939f729e85db1848911f3f3e61704'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='a216441b0aeba416ff109cf7eb4337ce00c7f4eba5e77b0b45a1b79cde736690'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c97ba455f72c4b9550669d799203255ec34da7f4519a6d13f6f66ccd3e2d8d`  
		Last Modified: Tue, 13 Feb 2024 01:54:00 GMT  
		Size: 1.6 MB (1581841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc9add719819af610dc87fdf0fc8398ff71903b7fbf67ec51397f54e5a7ed4c`  
		Last Modified: Tue, 13 Feb 2024 01:54:03 GMT  
		Size: 203.3 MB (203303294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-8-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:d4d50f9773f6876f18649c27b3d727238a3e4237a2df2203b75d75041ec0635b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822c45de6473f29f5c3f0e2f53788d85db5c517b9d60d58d958c5e19b9e942b8`

```dockerfile
```

-	Layers:
	-	`sha256:c110a6511c1ab669d4b31be48cee8f64ecef10710c33a30c906865ecb2de6e33`  
		Last Modified: Tue, 13 Feb 2024 01:54:00 GMT  
		Size: 2.3 MB (2281954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de35f4fa529053699d9e5168c6b6f22f18e5760b1dfd357d186c3fd9a470bdb8`  
		Last Modified: Tue, 13 Feb 2024 01:54:00 GMT  
		Size: 17.5 KB (17459 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-8-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2dd278e4044a3582db83250cadd61a1746beba7ace8b917c923c002f45d32900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232822111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe1b84a60cdb8720fc1172a2b0587d1eb8ac7fe1a1aab8fcfe1b2582fe5d30a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 02 Feb 2024 19:54:38 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 02 Feb 2024 19:54:38 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:54:38 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='3f36f003a7dbc52c00e66678dfd2c190be7939f729e85db1848911f3f3e61704'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='a216441b0aeba416ff109cf7eb4337ce00c7f4eba5e77b0b45a1b79cde736690'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66665e7107836c004c0e092f793e4525c11b530024a61f362798cc6f7500ab93`  
		Last Modified: Wed, 14 Feb 2024 01:18:12 GMT  
		Size: 1.6 MB (1565944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f718802620c0256d6b9555425f3b00f226bb90f4870ed40b4c2d0341756f94e`  
		Last Modified: Wed, 14 Feb 2024 01:18:17 GMT  
		Size: 201.2 MB (201185090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-8-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:a0d33ea2efd534c781cf76f1a186408768c3d856891bacf4fed18e839cef4d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570c84d5693e1660d53c28eba848334bf20f6b5fe2ede45029db62868c999148`

```dockerfile
```

-	Layers:
	-	`sha256:65cfb4c2a056abc25cdf78f00cf8865997126562e3a40970e396fb3d5ca7dd96`  
		Last Modified: Wed, 14 Feb 2024 01:18:12 GMT  
		Size: 2.3 MB (2281316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d148e6a69993c0a7395e28142d957feb0794be838fb918ec6516b1a0d14cf039`  
		Last Modified: Wed, 14 Feb 2024 01:18:12 GMT  
		Size: 17.3 KB (17305 bytes)  
		MIME: application/vnd.in-toto+json
