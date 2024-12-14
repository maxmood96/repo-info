## `openjdk:24-ea-28-slim-bookworm`

```console
$ docker pull openjdk@sha256:33556a98ac24a45a894ad8ad9bbf11ce1781adb0481c6898b06114d0e43c8d1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-28-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:5c5f34e2c638bccdb07fbc975eb8c3b032b34d9e909148a557bc564a6664b5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (244968801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec49a788b595f2d2c9b835e025cd8ddaf8651b8f1e6cef5151bf42cf3ce4642`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 13 Dec 2024 19:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_VERSION=24-ea+28
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='3d1038a0c6dfc0821d81a3995a1ce7225c5c1c97413c38e3ba76aba3562b4192'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfc242be61e5de4a8b5a38551bb2d0e17e3308b9e260583cc4db5a54f6c91938'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d7efba201ac6cb26ee68550845b3337b2f3bf81ec3325bfcf91eb3a7bf84e6`  
		Last Modified: Sat, 14 Dec 2024 00:30:01 GMT  
		Size: 3.8 MB (3824691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123299ad29a289da56550daadc8d987d9ac16d9e80d63366a8def64dc107c821`  
		Last Modified: Sat, 14 Dec 2024 00:30:04 GMT  
		Size: 212.9 MB (212912530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-28-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c8f34c98dd9e76d5aaca86db4a5851bd857ca4e6d6183b7bf25feb1b7ac2ab46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2556212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722e1a4e2f67a0a7fd884452c429e31130f2464874fe4f9d6cd0f0a707840b1f`

```dockerfile
```

-	Layers:
	-	`sha256:59b5270a01b5788ab1971ab8694d66babf29c1402daebeef4665a4e0bfa6bd03`  
		Last Modified: Sat, 14 Dec 2024 00:30:01 GMT  
		Size: 2.5 MB (2536770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee1a46eae940f665e45a3b4c0eb39203ee613f9a4ef7ff7e397153293a970427`  
		Last Modified: Sat, 14 Dec 2024 00:30:01 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-28-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:442e84f80dcc75044415210ede3d5978fac73bdded75c465d57d118deeaa3dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242574518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fefe882a4d30500d2962769612b1cdb669cb894eedd5b990ab7f413235d8b1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 13 Dec 2024 19:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:48:13 GMT
ENV JAVA_VERSION=24-ea+28
# Fri, 13 Dec 2024 19:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='3d1038a0c6dfc0821d81a3995a1ce7225c5c1c97413c38e3ba76aba3562b4192'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/28/GPL/openjdk-24-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='bfc242be61e5de4a8b5a38551bb2d0e17e3308b9e260583cc4db5a54f6c91938'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40c9250855fd1a37d1e80a3326b38199c756c64aeef5dcf30f8c09d2e6bfeb0`  
		Last Modified: Tue, 10 Dec 2024 01:29:42 GMT  
		Size: 3.6 MB (3639399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e9e5d80fbc5b57ff640b501d4a4e6770730506970913e46210c17df7c5e358`  
		Last Modified: Sat, 14 Dec 2024 00:37:50 GMT  
		Size: 210.9 MB (210876309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-28-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3d87875107a893e46a2257afc0aeff811046197bc95048e4b25ba488c8dd9a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2556155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4330c420b2dc6674d205130ced1eb969c4b7f187dd804b49692f49e2d742f56a`

```dockerfile
```

-	Layers:
	-	`sha256:1dd07ae590535047ac0df1659f44407f82d6cd4f3a66a7db4e19b00a85c2c470`  
		Last Modified: Sat, 14 Dec 2024 00:37:44 GMT  
		Size: 2.5 MB (2536498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e775f76969f788b17c95f22261541c288648a895d36aaa557f1ac257d244492`  
		Last Modified: Sat, 14 Dec 2024 00:37:44 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
