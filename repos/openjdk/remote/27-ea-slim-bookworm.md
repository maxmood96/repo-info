## `openjdk:27-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:d5011912b13fb63a5ba58f04ece230f48e86293220d073b9c72eb2f8002c83f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:24171667cc746380b7ad76a06d15d0b98e049f1993a88d3232939e198237dbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259386141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8438ee53f2aec9d58f98e8c590b518c86a6aaef124dcfccbb9d888540a030ebc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:32:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 16 Jun 2026 23:32:13 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:13 GMT
ENV JAVA_VERSION=27-ea+26
# Tue, 16 Jun 2026 23:32:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='8b55960efe73b9eb24c424f6d7dd1dae088eb2571c81dacfa76d05a2b9e24523'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='062f3bc3a420c426c85bac9a0051044a4ce17a8f67b382efbd3f5406cb9c184d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190dddeca9b9fd1fc1cc5253dbe2f0cb4d622d53f5b45cc774f0a9061661a0b8`  
		Last Modified: Tue, 16 Jun 2026 23:32:34 GMT  
		Size: 4.0 MB (4032948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764efbdab2521ed09f07e0239a26c8b5bedb787bde3808f041fcb7a3827c403b`  
		Last Modified: Tue, 16 Jun 2026 23:32:39 GMT  
		Size: 227.1 MB (227115569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:8856d2b014fa33a24bad6d7f3cb0bbb6310d7ad96fabf5381ecdb7ca8c8a2123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2664159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63034c4900a0bc0d69b30a42218bface5bc7bdd1f10e98c85ad384871895ddda`

```dockerfile
```

-	Layers:
	-	`sha256:a16860167a0b00a0cce19796474604df3779937798d13c04b07d0c5f35812412`  
		Last Modified: Tue, 16 Jun 2026 23:32:34 GMT  
		Size: 2.6 MB (2647290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db8a7a522a6a13e44c5ea9f8bf1059127c9dc43aaebaaecf59098cbfe578b722`  
		Last Modified: Tue, 16 Jun 2026 23:32:34 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3f922da6e4e7bc723713e4eb0f3d792cb731d1127cf987407515167e73139e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257072172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a747deaeb314b19f80ac6c4dc91628c65d2ba3692b24d16fc0347903ffabd380`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:31:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Jun 2026 23:32:04 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 16 Jun 2026 23:32:04 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:04 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:04 GMT
ENV JAVA_VERSION=27-ea+26
# Tue, 16 Jun 2026 23:32:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='8b55960efe73b9eb24c424f6d7dd1dae088eb2571c81dacfa76d05a2b9e24523'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='062f3bc3a420c426c85bac9a0051044a4ce17a8f67b382efbd3f5406cb9c184d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038ca80f78ce9e186ee9f16374c96d6bc879213098b11e3a396d62a4c1cc2593`  
		Last Modified: Tue, 16 Jun 2026 23:32:25 GMT  
		Size: 3.9 MB (3852830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad093cc118537b6cee4669d2747a8eeb155a2cc2370875a5846457e78b240f5e`  
		Last Modified: Tue, 16 Jun 2026 23:32:29 GMT  
		Size: 225.1 MB (225097035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2e43ba2d6088817d4bdd68cde68d67d4311d861fe0d894017c696eec1b2be3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2663914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3551ec8c580f3ab0fb50064f53c7f2f2b6d97a9cde1c7c5e9f6f070d124f34c9`

```dockerfile
```

-	Layers:
	-	`sha256:de8e3088d1ee6fd366bd329130e2bc8d6e7bcd272d01af6f8eef75e2f79355a3`  
		Last Modified: Tue, 16 Jun 2026 23:32:25 GMT  
		Size: 2.6 MB (2646924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ac965b54010d06b26c18734f1e69eda4199cd1be29ab512f76758faf022e7e2`  
		Last Modified: Tue, 16 Jun 2026 23:32:25 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
