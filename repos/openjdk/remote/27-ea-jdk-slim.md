## `openjdk:27-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:0d7b027b083fd41866fa09f59f80c3101234a68fe682a10ed46dd75d408703c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:911a8d7098a05dbcc92ecdcd3c4f44018b71773bceacc04e2d33a328a03d1989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260747480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2772122a8f4e58dfc0e29c9c82c11239d04b1d65ddc716e95c86579e4a5220`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Tue, 28 Apr 2026 23:34:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:34:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 28 Apr 2026 23:34:38 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:34:38 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:34:38 GMT
ENV JAVA_VERSION=27-ea+19
# Tue, 28 Apr 2026 23:34:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 28 Apr 2026 23:34:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62c0fde740c79956034d2a0c48bfdbc7a2908395904bb89dd1d3f67c46e54bc`  
		Last Modified: Tue, 28 Apr 2026 23:34:58 GMT  
		Size: 2.4 MB (2371114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ba62b3078f1bf45141dae067b6e6ee93a8160ee9202a6152e01478374f89cb`  
		Last Modified: Tue, 28 Apr 2026 23:35:03 GMT  
		Size: 228.6 MB (228596192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:f860f23e5b937a837381e0067d8e6395fc8406022f1face61fd83fbaee66c1f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d51b2df99f4a95c38601ba5ea9db86bbf308f75b2f8da7975fd18fc4b36c757`

```dockerfile
```

-	Layers:
	-	`sha256:f3cc5512f44f6d2b5a87bee5a8bb592e492408e7814884bfc7b87eb7097bed01`  
		Last Modified: Tue, 28 Apr 2026 23:34:58 GMT  
		Size: 2.3 MB (2277625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:363c34113dc86b9b9b15fd9093ec2d1844b226bdfbe9dda34c193137ea0b7792`  
		Last Modified: Tue, 28 Apr 2026 23:34:57 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:579e48a52e486de6934ceaa8ab7d77ef73b8b6251bca6e860434d1e340f53894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (259009384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b0c6428256646b90c1afe2139342dfb4cdc262e3184f33d77e3dea89420f94`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Tue, 28 Apr 2026 23:35:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:35:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 28 Apr 2026 23:35:39 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:35:39 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:35:39 GMT
ENV JAVA_VERSION=27-ea+19
# Tue, 28 Apr 2026 23:35:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 28 Apr 2026 23:35:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae31b7b69c8a3fc05f8d90186a31a963572482e02dd96c0ae3a3b59e70a615b9`  
		Last Modified: Tue, 28 Apr 2026 23:36:00 GMT  
		Size: 2.3 MB (2314392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d123c9ade1befe9ec4c4140aa195d4e0c24329895fd6e81b1856e1ed64961e`  
		Last Modified: Tue, 28 Apr 2026 23:36:10 GMT  
		Size: 226.6 MB (226551386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:193ab80e92af1b0021dd415821ed8a8949a4b0bc9d0e1ea8fb50b2c3eda567e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228194037bcadab82189e25341ca9fbc771cc212ab82221304a1545cbe51f2c8`

```dockerfile
```

-	Layers:
	-	`sha256:887fb9264fc499f53c1195bc3ab6c3aa2167fc2378e6f24f89e4be5144cf6700`  
		Last Modified: Tue, 28 Apr 2026 23:36:00 GMT  
		Size: 2.3 MB (2277311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:670ae094fb2270c5ae5cff5c384ce0a564e5b06bef596fc82bf9b44c8e1e3c41`  
		Last Modified: Tue, 28 Apr 2026 23:36:00 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
