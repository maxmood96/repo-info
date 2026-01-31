## `openjdk:27-ea-7-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:1f7a435639a6f098362d9bbe3c66c6a0d6851cf434423bd93bf7cce5ecc93ed1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-7-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:54c9bf01201787dd9c863bd9dbb301422c42138c9de66dbc8ce02f76396f1d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260663181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851da50e4e47cc9df22fdc807adfa477e811f25d68458633f0946833a549b348`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 30 Jan 2026 23:40:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 30 Jan 2026 23:40:31 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:31 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:31 GMT
ENV JAVA_VERSION=27-ea+7
# Fri, 30 Jan 2026 23:40:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaa949940f77d14d76528d472dff84b61653eb58f64d7e6a38a93da5ffc000d`  
		Last Modified: Fri, 30 Jan 2026 23:40:50 GMT  
		Size: 4.0 MB (4029184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb46fb66675a56295fb10a424aa244c5a7c313678185355ccb4429249b824345`  
		Last Modified: Fri, 30 Jan 2026 23:40:54 GMT  
		Size: 228.4 MB (228405425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-7-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:1dd27a103dc27357346c5c07c6a76bda7e8312ee6f933ee913b109ef3ad67e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cf4fd66850f06c4676ec196e563c00158931d351a49a68e20193afdafdb3e7`

```dockerfile
```

-	Layers:
	-	`sha256:26b13c92c1f803c22dbe2199a546292b6bf0743147b96f067151df4b12320a07`  
		Last Modified: Fri, 30 Jan 2026 23:40:49 GMT  
		Size: 2.6 MB (2649170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6273647cf6db51d49e3a1b62526fedb6fae7c6051e9ec65cf74d3fadf07f80c8`  
		Last Modified: Fri, 30 Jan 2026 23:40:49 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-7-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ae7cc8e82813ddf08ad82251021ba456db884912df586a2134658ff40a41a613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258304306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d153691bbd06f486b5fe077f9fa7a819103817702b9c73a89d0ce082904be2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 30 Jan 2026 23:40:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 Jan 2026 23:40:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 30 Jan 2026 23:40:44 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Jan 2026 23:40:44 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jan 2026 23:40:44 GMT
ENV JAVA_VERSION=27-ea+7
# Fri, 30 Jan 2026 23:40:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 Jan 2026 23:40:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9804f47d151b0703f379af20af481380b6ac60f384b423449a46fe7d8d4921`  
		Last Modified: Fri, 30 Jan 2026 23:41:05 GMT  
		Size: 3.9 MB (3851987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a3a5500426ea7c0b7d7f0c1d77548167ba4b8fc4c4691b1f0cbf4e02fa0df3`  
		Last Modified: Fri, 30 Jan 2026 23:41:10 GMT  
		Size: 226.3 MB (226344430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-7-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:dd16940bef68ff29e76fba4089a0af9886719d78dc8cfefd6657481f8052facf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a287038a7a4971f85c7eb21b56ddeb1c2cc7c375a562515fb493fa5fb192265`

```dockerfile
```

-	Layers:
	-	`sha256:bb12c4f6b9420099d554f2ab378286786f0d173a8623d2665e258d96d6b85fb5`  
		Last Modified: Fri, 30 Jan 2026 23:41:05 GMT  
		Size: 2.6 MB (2648804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43031b9cf6ba8a42da6188e76e167be136ea36c1007e6155f2b424b05ca61c9b`  
		Last Modified: Fri, 30 Jan 2026 23:41:04 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
