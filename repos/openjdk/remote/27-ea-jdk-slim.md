## `openjdk:27-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:5288c665628a22564ba0e7a5681f32774c5a65164b315cdb56a94e674c120904
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:ec38614a01ef6eedf74f08bacaaf894bd825748497264c55b9fbe6f7254c288e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260198350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce704d3fb1ef4bab44997a8d4d956145ea8b760049e97b44e6784f9eb743507`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:17:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:17:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 08 Dec 2025 23:17:36 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:17:36 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:17:36 GMT
ENV JAVA_VERSION=27-ea+1
# Mon, 08 Dec 2025 23:17:36 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 08 Dec 2025 23:17:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923c21c21ac938c8f8c478687030387ec387a81bd46f888bad7be82b326e1f55`  
		Last Modified: Mon, 08 Dec 2025 23:18:08 GMT  
		Size: 2.4 MB (2370986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b261c5df3a14e1c34709e8f11f8e741f21e2136c11510196c3d32ec9029066`  
		Last Modified: Mon, 08 Dec 2025 23:20:29 GMT  
		Size: 228.1 MB (228050868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:a1c424942f35407ed69c223d7324fb15836d3a22686e4ece220a2e4c5b1d3c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f9e27dab21287d94f67cc5bb4360ed0f965a5756761f61ed8e045e5916ce1b`

```dockerfile
```

-	Layers:
	-	`sha256:86829ff4b31f0c102b4e5a71ac7214e111f955f99011effa20330e6945af9fb1`  
		Last Modified: Tue, 09 Dec 2025 04:25:11 GMT  
		Size: 2.3 MB (2278773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca4cff563ae49f40b536ff8c041abfe0d00ac943d6c62e6f1d7c2e73f7203055`  
		Last Modified: Tue, 09 Dec 2025 04:25:12 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3f17fa425c0bca4065886c9bcbe6473cbe608623f16e28d30fafc9132e4a70b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258416928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eea1c31a21063fe3701f09374b160f19a6fbce892141c20d533108045edd153`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:21:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:21:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 08 Dec 2025 23:21:18 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:21:18 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:21:18 GMT
ENV JAVA_VERSION=27-ea+1
# Mon, 08 Dec 2025 23:21:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 08 Dec 2025 23:21:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fb262f4fb72417f8d60ef1ed0f44c76a6bc5892f83babc475eaa3f2cd31162`  
		Last Modified: Mon, 08 Dec 2025 23:21:48 GMT  
		Size: 2.3 MB (2314146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede0b8bf3500318c2185ae0f4cb03015519d669f81e10f876fc6ac6dda9cb793`  
		Last Modified: Mon, 08 Dec 2025 23:22:06 GMT  
		Size: 226.0 MB (225964154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:06d448ae7853ec1dc47358b6d2f7cadabb6fe2f15df73c4fdee591abb76f6049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121cd5fb40676b137734a9785f8f2649cb7e96b9f9fa7d59c23ab3f94518b899`

```dockerfile
```

-	Layers:
	-	`sha256:ca6f58cb8285f8d6a08c89e2b0c96fd3f413e29cf9e6ddef8618862d3c9cc64c`  
		Last Modified: Tue, 09 Dec 2025 04:25:16 GMT  
		Size: 2.3 MB (2278459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f335f10fe9dda4ce0eb1289a1e48073626e2236dce522a0180b5195af4491d97`  
		Last Modified: Tue, 09 Dec 2025 04:25:17 GMT  
		Size: 18.3 KB (18253 bytes)  
		MIME: application/vnd.in-toto+json
