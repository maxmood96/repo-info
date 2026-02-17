## `openjdk:26-rc-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:f6b3da9a36bf8cc41e9a4a39acd8963609909de89087c44ddb0d01c12acaf895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:85da5beee8aa9d9899834b223e550c70e05c464ffe9fbba17293d5e76195c655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260364073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e616dcc4fb029caa311c64d58147649fe3e9c8e312632cfaeb31512babdb71e0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 19:31:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:31:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 17 Feb 2026 19:31:39 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:31:39 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:31:39 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 19:31:39 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:31:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbad095f90d292525a49a31433fc731ae5cf4013b75cb10b669a422c1d4d918`  
		Last Modified: Tue, 17 Feb 2026 19:31:59 GMT  
		Size: 4.0 MB (4029223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e4f872c9cbc02b394c9407c545efd7ca8a702e0479cc0a81a4274c62a5c22e`  
		Last Modified: Tue, 17 Feb 2026 19:32:03 GMT  
		Size: 228.1 MB (228106363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:92327111dd657c6a6e06fb190ee260be9a552ec1e7145ccb4a2f7030f7c37612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8fb3ee49767b4f03fad32291a17483fcd287f8aebd5ce003f8e2a93baa12e90`

```dockerfile
```

-	Layers:
	-	`sha256:70e058389dc1da3be08bc340e5592559114cf8918c76d2d7a45f8dd0d6a71655`  
		Last Modified: Tue, 17 Feb 2026 19:31:59 GMT  
		Size: 2.6 MB (2649744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67952b201a8cf89fe981f53fb4903d067ec38ffab1b96cae39a72faa96d0fead`  
		Last Modified: Tue, 17 Feb 2026 19:31:58 GMT  
		Size: 16.3 KB (16267 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fe5a082c53b1586e21f6b0f9c2b3bba732b7aeb6f31bc1e2fda0d0754664570c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (257989494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6eb5d75de8e42c86d6f89c97cd78bf4d47ede68fb981b7d3c3a7063188e3d7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 19:30:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 19:31:02 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 17 Feb 2026 19:31:02 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:31:02 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:31:02 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 19:31:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:31:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b8f1f347843a1a26934a354c34cb3bd6be33232fe7d083d580ca58cf6476b5`  
		Last Modified: Tue, 17 Feb 2026 19:31:22 GMT  
		Size: 3.9 MB (3851936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f304594753088196c9619f0a78e568b7703fe02e9b70faae395865c799d2e7df`  
		Last Modified: Tue, 17 Feb 2026 19:31:26 GMT  
		Size: 226.0 MB (226029735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:93a0f0c54314816cb81255672e464ddf31371e965127672d52bced8e9eca6f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a344c3141e3ec347df6b239295d27feb7563e3c2a46a992f0d4ef1df9a7d266`

```dockerfile
```

-	Layers:
	-	`sha256:b82c05a2d582d03563bb0ca891b4188a68a137207ce846aca1d5be27deb3546a`  
		Last Modified: Tue, 17 Feb 2026 19:31:22 GMT  
		Size: 2.6 MB (2649354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d80bb06b1bb103434b283e33c84f8ff6ac868e9aa899372127eb6b81b3ec5c`  
		Last Modified: Tue, 17 Feb 2026 19:31:22 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json
