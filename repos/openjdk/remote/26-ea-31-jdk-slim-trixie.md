## `openjdk:26-ea-31-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:e174cbe25230abdcc2fcd5e5ce834d6d7e5b9fd1daf6aab6e35f647d3b0475cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-31-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:13929492cb8a6d974eb39a6b0c26f861d27ff2b65412e2b89df0ae71bc32bc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260156033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cd0f5cf34f0ecc76dac884421f7fe732f4933ffe38c362e638cdcc918010a2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:46:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 20 Jan 2026 18:46:52 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:46:52 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:46:52 GMT
ENV JAVA_VERSION=26-ea+31
# Tue, 20 Jan 2026 18:46:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='bfc006ca65cf590a40d808e5dc5cc973b98e11e309d0efa5dc36340c8b3ffdbb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9511be1b72db3be1c49c25cbecda90f37642003c9844f7d363455ad702ff7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:46:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bda8ee697b8dbbfe2f91e296446db78c346a2d1e7603e894d0ce5a0c377404`  
		Last Modified: Tue, 20 Jan 2026 19:27:22 GMT  
		Size: 2.4 MB (2371073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3b56e0c2ccbea56b035610893a6dabe0c566a0a85fbfa68329191b1896bd11`  
		Last Modified: Tue, 20 Jan 2026 18:47:16 GMT  
		Size: 228.0 MB (228011275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-31-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:9b11d04bfd6d6de08e3a8bf06be4fe6d81feb0829660da8ed3ee012d97e81410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bff7de7f29817cbfb0c51e7ab1601aeed4d9c6f54e4f69a933d1158a90243df`

```dockerfile
```

-	Layers:
	-	`sha256:4f25d35bca60a9358a285c57e6789ddfa6039b6039bdd4352185b7a22a6554c9`  
		Last Modified: Tue, 20 Jan 2026 19:24:03 GMT  
		Size: 2.3 MB (2278851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7293a2188e078f512b99f5833fb57c983eb35a0ba7795c3ba0e341c93852a928`  
		Last Modified: Tue, 20 Jan 2026 18:47:11 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-31-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9e0079eb920febcd43284f2920904d4bca8a72e93c1bd55f516600879bab9dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258384662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415988c61af41dfacec488d244ae0f1c216b71a2dd0ae99a11479d1d61f5ba92`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:45:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:46:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 20 Jan 2026 18:46:16 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:46:16 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 18:46:16 GMT
ENV JAVA_VERSION=26-ea+31
# Tue, 20 Jan 2026 18:46:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='bfc006ca65cf590a40d808e5dc5cc973b98e11e309d0efa5dc36340c8b3ffdbb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9511be1b72db3be1c49c25cbecda90f37642003c9844f7d363455ad702ff7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 20 Jan 2026 18:46:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5827ab8c83a3790b248805517a48f6dd6513615968f6acc4873aab2e8486e3a1`  
		Last Modified: Tue, 20 Jan 2026 18:46:37 GMT  
		Size: 2.3 MB (2314132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8171d5a729cb2fe01b61bd194df47edeebddc4d05293478efc438ccf78a0def`  
		Last Modified: Tue, 20 Jan 2026 18:46:41 GMT  
		Size: 225.9 MB (225936488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-31-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:f119cdc0c4f9b148b81b4729be7124f2024748b2ba53bf6b979a9e0f284fb2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8df36f8cf3590d2c3ffc86581ba8a4ae7661680bdd1317b3959afad93f62295`

```dockerfile
```

-	Layers:
	-	`sha256:4b31a2e3e1445eebca574b2e8d8110c26d79ab0beb2b478555e678663733313c`  
		Last Modified: Tue, 20 Jan 2026 19:24:10 GMT  
		Size: 2.3 MB (2278537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a39505c743bafc6a02c8c6d531b0fc46ae6e94c69337b1d3fe346d665087d6`  
		Last Modified: Tue, 20 Jan 2026 19:24:10 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
