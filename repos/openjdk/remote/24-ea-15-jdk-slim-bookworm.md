## `openjdk:24-ea-15-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:7d30974a2c31d98854c3296a21999116d55825d3a65cc6583f700e827b891184
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-15-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:72540e8aab9a65c7643378b3c3349a992f0ad01951215db503a2e8685c0b5b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242859289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f437ea865506911f79a47664d0c0784abf0810fc16629c7fdd4b43537bd59b3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Sat, 14 Sep 2024 06:48:15 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Sep 2024 06:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_VERSION=24-ea+15
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='b41d4867c348d7f1991085d8bcc8797eaf032d9dfaa3419bc9db15eaea75e91e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='165b7c19403e9708ca261cdfe4c385e837df683049203e33ad2bf76228054a25'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f55d71591737b02292699c3b818022d57eb096a05e70b2db7daa5f59a52e15`  
		Last Modified: Mon, 16 Sep 2024 19:23:27 GMT  
		Size: 3.8 MB (3833454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d81fef4028184e0f9bba22a8162b51302ce56a64345198f3747c486c80ecb6`  
		Last Modified: Mon, 16 Sep 2024 19:23:32 GMT  
		Size: 209.9 MB (209869290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-15-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:aa92b1c1d1cfd3d84e427f85d1d5fe805ed950b2c12b462b2410db2ad564583e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa96f363275611df1be207efe361b2257d1f57b29cea726babfddfed96f3686`

```dockerfile
```

-	Layers:
	-	`sha256:8de94d28f7656aa791f2e05e0811df696c3435cca9b91d14f78d5915817bfc10`  
		Last Modified: Mon, 16 Sep 2024 19:23:27 GMT  
		Size: 2.4 MB (2365660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d5de06b9f2cb12648b8f6117ecef97bca240c2a5a55c85ce6dbe1bbc387e05`  
		Last Modified: Mon, 16 Sep 2024 19:23:26 GMT  
		Size: 19.6 KB (19635 bytes)  
		MIME: application/vnd.in-toto+json
