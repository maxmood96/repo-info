## `openjdk:26-ea-23-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:539ccfa227f8761456f41c9aee0bf729709d8d27b982ebb09405849ff26ff0e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-23-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:0b65abfa7e9bc8c9ffbcbd139d0b8661aee163a9c4aaa4335cb329cc556e7457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258160841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c456def54c1cfa58e86c3800c470787c45029587f54631f50484d2e9045ddd1b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 19:52:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:52:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 10 Nov 2025 19:52:25 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:52:25 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 19:52:25 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:52:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='c5cb587a920ddf65225352cf2494965786acd1de8d6748a976d7498d0783a396'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='427f53a6635347b853f695324253b6d78f69cc09334a9cb1031a801e43358883'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 10 Nov 2025 19:52:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb7ab116279210c1995e2c45ab14efd4ab132e048160c1d46c0a3231c5938b6`  
		Last Modified: Mon, 10 Nov 2025 19:52:57 GMT  
		Size: 2.4 MB (2371190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413b0aae1cf01ba335d3e20cda8b1554a4cdb9b57d1ad9b29dee07379d2d8dc7`  
		Last Modified: Mon, 10 Nov 2025 22:29:34 GMT  
		Size: 226.0 MB (226011547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-23-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:f97c64e3b5bc88515be81d6feb1204ac0f38e2a679bcd95254ae2729b41bb31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cca6c4ec6c755e1963cbd339b85896547e8cfd3771d0c1c730c141da1f46c5`

```dockerfile
```

-	Layers:
	-	`sha256:77ec36de25928d63a96bb4fee5eabd870cfa25cf3b1546628516638cc3d90497`  
		Last Modified: Mon, 10 Nov 2025 22:24:08 GMT  
		Size: 2.3 MB (2278795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2434ea51ccb9f6c30cdc3188499f29ea6bb88e167527bc95ad88ffff950c57d`  
		Last Modified: Mon, 10 Nov 2025 22:24:09 GMT  
		Size: 18.1 KB (18108 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-23-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d89ed1d31e848874fdebf3b64c0744086e62b959f9f5a9a946452a6fdc7ff6b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256316941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba1cab0a4d564d7e2d4a4a93c6a6de95ea61187e7823be469bc0e7bd888ef2c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 19:52:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:52:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 10 Nov 2025 19:52:58 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:52:58 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 19:52:58 GMT
ENV JAVA_VERSION=26-ea+23
# Mon, 10 Nov 2025 19:52:58 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='c5cb587a920ddf65225352cf2494965786acd1de8d6748a976d7498d0783a396'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/23/GPL/openjdk-26-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='427f53a6635347b853f695324253b6d78f69cc09334a9cb1031a801e43358883'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 10 Nov 2025 19:52:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b25c56e2f73e11d20e7fdd6328c1e0db9d82d2acedc71a70f446a61e0647924`  
		Last Modified: Mon, 10 Nov 2025 19:53:31 GMT  
		Size: 2.3 MB (2314262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a4341f72b23fee42d02d82f12443ae9195d3fae88a2cb5f2cc7d11a255f5ea`  
		Last Modified: Mon, 10 Nov 2025 22:50:16 GMT  
		Size: 223.9 MB (223860381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-23-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:b72ed9b791ba62974673b800532348509523ad3d41b2aff056108a78f620772d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9154732c78742adc063bf7d4313cef3988d3cfe56c7336f17be92c07abb3367`

```dockerfile
```

-	Layers:
	-	`sha256:7ca2012456f590c46ef4b021851ad208f5c0a33d97f395eb53d9402b874c4ad1`  
		Last Modified: Mon, 10 Nov 2025 22:24:12 GMT  
		Size: 2.3 MB (2278481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f5bbc8b34f3b80a415c4489fe4be0450d8a6eda4b8393bbd8213a5195826529`  
		Last Modified: Mon, 10 Nov 2025 22:24:13 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
