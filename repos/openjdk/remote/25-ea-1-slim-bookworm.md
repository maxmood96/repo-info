## `openjdk:25-ea-1-slim-bookworm`

```console
$ docker pull openjdk@sha256:b115c925cfc93e3919f448d9ef0a6bf4aaf16f0c615adda917cb535552d2c95c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:25-ea-1-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:f7a2434d652079ce45ef465f84f3ddd37f723ba09f70991b7f00978e1c1c6cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245082935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04342d1fe65a0c9432a4aed862ea6440677297a5ee7ba0d66e51366384097973`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Mon, 09 Dec 2024 05:52:24 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 05:52:24 GMT
ENV LANG=C.UTF-8
# Mon, 09 Dec 2024 05:52:24 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 05:52:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='b2c1c3716a21ae204e31e0f37782552ffef0f6e0d9850ba16fb57cd0fa98d84c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='76761c3ad2bebc865c5ed4ce08a7c5f89eb4f51d3f471d76f650e0556d79daa3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Dec 2024 05:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb47715aa17aef8c81c57ad73b3fb18614371def74c2a4c89d43b0da5b28aa5`  
		Last Modified: Mon, 09 Dec 2024 23:30:25 GMT  
		Size: 3.8 MB (3824707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e59257e1315400ac595c26ef9551469aaf1f9f5e1cb4e6bcac15b5fda605ed`  
		Last Modified: Mon, 09 Dec 2024 23:30:28 GMT  
		Size: 213.0 MB (213026648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-1-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:fda3a77612fde1becc6b3ca134a4bed16a94427656ecc00a2d317786447ed1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2556179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cee202a26f2a04dd2a849b3a3c9e225b8999d46c8d355de85430bc70a4d787`

```dockerfile
```

-	Layers:
	-	`sha256:d27885aed4c3899c4595312e56e6b39c61e8bdcdcdd9092c3f2d72dcba87e002`  
		Last Modified: Mon, 09 Dec 2024 23:30:25 GMT  
		Size: 2.5 MB (2536754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df17a0c48beb66b736afc8d04b8a27af939c4331cf7cca3cdec257c6a5f545eb`  
		Last Modified: Mon, 09 Dec 2024 23:30:25 GMT  
		Size: 19.4 KB (19425 bytes)  
		MIME: application/vnd.in-toto+json
