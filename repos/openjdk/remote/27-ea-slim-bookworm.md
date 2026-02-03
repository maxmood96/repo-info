## `openjdk:27-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:e26563d9fbee722f0d5c1f278cb8eca6faa6d547f790ebc15fb2c354bf3075ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:7b8f2ec34074c84c53b9f8188c0d0ea87a0a38c4ba5ec7a1c548dd3c1eb1cf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260663033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2824118be95ed1e0ebc9348ff602f11772222b9259f46851952de75d6ece18af`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:50:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:50:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 03 Feb 2026 02:50:46 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:50:46 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:50:46 GMT
ENV JAVA_VERSION=27-ea+7
# Tue, 03 Feb 2026 02:50:46 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 03 Feb 2026 02:50:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd34b0de2cfa752d2b6ef8bee598ee1cb9c8773d5be404de698e4c60b6144b81`  
		Last Modified: Tue, 03 Feb 2026 02:51:05 GMT  
		Size: 4.0 MB (4029125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ca84c9038ec97aeb7b3ae68d678e5519f9ded165266bce108efdab2e277e7`  
		Last Modified: Tue, 03 Feb 2026 02:51:10 GMT  
		Size: 228.4 MB (228405421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:9a1e26356dcec88b7286cbd295f459e21f37d518866b2adc2d210a147bbff036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab7840233c2725dcdffdbb28f32b2893d008a54a611262bd6a152895c15837e`

```dockerfile
```

-	Layers:
	-	`sha256:becbeb5d8dfa5e2938767d730c64b1a1f21cb4863553f4c39cef6bd3c945c333`  
		Last Modified: Tue, 03 Feb 2026 02:51:05 GMT  
		Size: 2.6 MB (2649170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfb585db58d9577e6fc89ad16f1eec22921f545ffc073e3cbfddbaa1b1c2899d`  
		Last Modified: Tue, 03 Feb 2026 02:51:05 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-bookworm` - linux; arm64 variant v8

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

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

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
