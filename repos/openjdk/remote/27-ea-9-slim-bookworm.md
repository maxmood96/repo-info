## `openjdk:27-ea-9-slim-bookworm`

```console
$ docker pull openjdk@sha256:ba1257d77acdacbf0990ed43f80c2fae3ad54622eec7622396214c8ab3def279
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-9-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:7611000e814c7a330a9bef41ff3a3372be0b2e42226c716fb00a67591972565f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260794837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f15590d21f332a13241dcc59640b5c9268261365f1df4b47346e99ba926e8be`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 19:32:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:32:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 17 Feb 2026 19:32:32 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:32:32 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:32:32 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:32:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:32:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a073c1a7bfe91ab72aad2424d4daae464e2fcf61f0393827f046de4567757b32`  
		Last Modified: Tue, 17 Feb 2026 19:32:50 GMT  
		Size: 4.0 MB (4029214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9247b1ac9fc9639f93e330693cd4e5faae06973845c5dee34ddceed97124e9`  
		Last Modified: Tue, 17 Feb 2026 19:32:55 GMT  
		Size: 228.5 MB (228537136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-9-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:36cfe3847ea7c9927e2700a725e7c77a3965994eccbb467ffe24343c98a38347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9754d844f0c85770b981e8affe4170488da4c7d059a05c09510746dbb5bfd591`

```dockerfile
```

-	Layers:
	-	`sha256:85edc691fe40e240259239dc522c9d91f7fefdff7cf87e18f015f3506445e4bd`  
		Last Modified: Tue, 17 Feb 2026 19:32:50 GMT  
		Size: 2.6 MB (2649799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e36ae7cb98c763afcf1f223634f24a63449d73f0d73bb6de81d08019cb158f75`  
		Last Modified: Tue, 17 Feb 2026 19:32:50 GMT  
		Size: 16.9 KB (16857 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-9-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:03f26b4022d77cd9feddb4b0391172dd6acbea356039a78b59f759b984711f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258444769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66516ffa330a3a20e807bc6226fe086181280de5a4aa35a9c4593d8a9c07419`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 19:31:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:32:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 17 Feb 2026 19:32:12 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:32:12 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:32:12 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:32:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:32:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0eb9b7e8e8dae0cb0f067d8deb72b19e87b0d9f8e18239613db045858a3eb55`  
		Last Modified: Tue, 17 Feb 2026 19:32:33 GMT  
		Size: 3.9 MB (3851946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88129e4564b63e42159318d9d6778d5cf00ad8d58c6ca18baa5085f9f2270664`  
		Last Modified: Tue, 17 Feb 2026 19:32:38 GMT  
		Size: 226.5 MB (226485000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-9-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:07486c7f23fda95ce7f39ec24d3cad97744abb2e62ea53c92afc276777cd7f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a06fa2151f98be4c87dc541186bae6d2a357be95a38864af03f26a91de87634`

```dockerfile
```

-	Layers:
	-	`sha256:7db443680bf35e30052306b249e63feb900f0e43e634e799c316df6ccbd9d17a`  
		Last Modified: Tue, 17 Feb 2026 19:32:33 GMT  
		Size: 2.6 MB (2649433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22ac90e251ccfba01c6e620e95641cca64bef62d6c8b912d259e1801034d73c3`  
		Last Modified: Tue, 17 Feb 2026 19:32:33 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
