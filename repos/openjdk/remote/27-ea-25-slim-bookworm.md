## `openjdk:27-ea-25-slim-bookworm`

```console
$ docker pull openjdk@sha256:a7770246962e087bacf5f1ce338b7eaa725ac72cf6a371286c2f09ca1733d297
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-25-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:5496da4d4788c2e43788bb643e3551a71cc140702587a55f5a20dce207b5d92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259390313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edca7c5287cb99a026f8a5a85b8ec05b94741c4e1f0166c9278d57139a5792c0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:47:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Thu, 11 Jun 2026 00:47:46 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:47:46 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:47:46 GMT
ENV JAVA_VERSION=27-ea+25
# Thu, 11 Jun 2026 00:47:46 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 11 Jun 2026 00:47:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec0f1f4ba508e1a0549b9f2d631a670b2d74988251d3157bbc09653b223c688`  
		Last Modified: Thu, 11 Jun 2026 00:48:04 GMT  
		Size: 4.0 MB (4032980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6eec516b2bea04c543600f80bd3aabd60a10c43cce30f97547aabc265a199a1`  
		Last Modified: Thu, 11 Jun 2026 00:48:09 GMT  
		Size: 227.1 MB (227119709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-25-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b2cbf7572ee4b33e2c106fec0604683db3d7dcd19e3a2893aa4f39855f91ee2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2664161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbb306c388a2e9438058cb1d2e9c447204935b8f5636de842e2e345a596e22b`

```dockerfile
```

-	Layers:
	-	`sha256:88248d649d3e61927042db7bd81991b35d276bbed08e7a1813747ccc8d01a726`  
		Last Modified: Thu, 11 Jun 2026 00:48:04 GMT  
		Size: 2.6 MB (2647290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbca5ac79b80f2f5aa0c0a0c4929dc92b716d33b4dcaf314195a73d35128d008`  
		Last Modified: Thu, 11 Jun 2026 00:48:04 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-25-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ed51416ddce7e92f9ddedfc9319bb7919902654f96ca4c593bd8f2169af93ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257071564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7a426c5cef14a0dfae8557b900b166363fc3632eb8b5b2d411476824dc9b2a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:49:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:49:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Thu, 11 Jun 2026 00:49:24 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:49:24 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:49:24 GMT
ENV JAVA_VERSION=27-ea+25
# Thu, 11 Jun 2026 00:49:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 11 Jun 2026 00:49:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c0a02e62cf0ee21630feae654b8f6451fc637f250667fd8728a790ad3b5c5b`  
		Last Modified: Thu, 11 Jun 2026 00:49:44 GMT  
		Size: 3.9 MB (3852854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfe3b6eed67d072bc7e102994c3113e493b75393ce3d1fe264cb8f4f750b954`  
		Last Modified: Thu, 11 Jun 2026 00:49:49 GMT  
		Size: 225.1 MB (225096403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-25-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:362f255c4f658744be8e8fdab64bd22a31fe50e6d41e65c2596f247ee6fc4f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2663914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affeb3f8c9d6101a237eb3337e8427319c8569f857a7d373bb238a1dc178a0fa`

```dockerfile
```

-	Layers:
	-	`sha256:58ab7c011833a0be0a1c96732bcc9a79405fe0a00758e28811835bad526b5b23`  
		Last Modified: Thu, 11 Jun 2026 00:49:44 GMT  
		Size: 2.6 MB (2646924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4fa8de40fe540006746702536088f1814d971f92c56f5d52159e9eaa9571975`  
		Last Modified: Thu, 11 Jun 2026 00:49:44 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
