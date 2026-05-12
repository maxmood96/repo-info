## `openjdk:27-ea-21-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:9b839261a429ba6f8b6c3f28ac440a18b12e8968c4110c99c37ea0f012e91183
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-21-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:20841896f60d52f4bab923ad7362384678fe1f1d5bd5a9d748156585438544c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261071212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b14039ac12d3b0ecbd294bc8d7aeaf1f8724c95ded5f40e464ec6bfa18a658`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Mon, 11 May 2026 23:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:50:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 11 May 2026 23:50:35 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:50:35 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 23:50:35 GMT
ENV JAVA_VERSION=27-ea+21
# Mon, 11 May 2026 23:50:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 11 May 2026 23:50:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bf22d3d86487d4ac38065f411b569d16a126337563db0c005da48e67e5377b`  
		Last Modified: Mon, 11 May 2026 23:50:52 GMT  
		Size: 4.0 MB (4030658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4435962784062991cb2b10e36742e29ad702c698683d9d85cd50d5ebaa7010`  
		Last Modified: Mon, 11 May 2026 23:50:57 GMT  
		Size: 228.8 MB (228804272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-21-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:3b1ab9cb8fbb25bf656dfa696e1d9e33195b858fc12609986c4c40dcb7a7af62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07bf943173512cb18963efddd065b2500218af34edf833a87004d96d7c21f6f`

```dockerfile
```

-	Layers:
	-	`sha256:d30f03feb670e39ee971b899b806fecc217e85f683f033f8e3b80e6895df0d54`  
		Last Modified: Mon, 11 May 2026 23:50:52 GMT  
		Size: 2.6 MB (2648537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b6e6b86e842c4c488f9b12ee553ebea40c4621647bd191a91a1ec8f37871f4`  
		Last Modified: Mon, 11 May 2026 23:50:52 GMT  
		Size: 16.9 KB (16870 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-21-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7c501889ed43b2293bf5e567adc308b67654c87915eb9af6755095af54737fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258742145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244725a6aee15c600d8b85177ecfc35ca622c7bb0905f2c85a27b76d695f2664`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Mon, 11 May 2026 23:51:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:51:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 11 May 2026 23:51:32 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:51:32 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 23:51:32 GMT
ENV JAVA_VERSION=27-ea+21
# Mon, 11 May 2026 23:51:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2982b468d0bc04eed44b9ca14f436488933734f32b0b64a2b993d37f2fcbe277'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='d56b552c9140a7a90e15122f9fa2cc8d472f7bab535fc473337d43c24be49ace'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 11 May 2026 23:51:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e08514a1cfbb356fae0c8513010e3f48a3200bb7a0ef8832566199edb8be07`  
		Last Modified: Mon, 11 May 2026 23:51:53 GMT  
		Size: 3.9 MB (3852185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af4a983e8c31c337b5e42cd7eaf54bf3d52b3e2a7d20ca1edb6cb5c03ae67a9`  
		Last Modified: Mon, 11 May 2026 23:51:59 GMT  
		Size: 226.8 MB (226773795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-21-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:73bd7ad00954f9d988647b7d39ca1eb7a8cc5d3bba2f4b898b3c29c151f6732f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6968dd77e95c660f2af00b1d53c553291272b8a2cd2d698f5f28d79514863b5d`

```dockerfile
```

-	Layers:
	-	`sha256:e762e02f2cf089816fbd60359c638b715d094f9b018d5e07dcafd0505ae19ecf`  
		Last Modified: Mon, 11 May 2026 23:51:53 GMT  
		Size: 2.6 MB (2648171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:028de645daf19c744c5aa5aefc02c779e202e8b7b21184692eb9fa31d25e91f3`  
		Last Modified: Mon, 11 May 2026 23:51:53 GMT  
		Size: 17.0 KB (16989 bytes)  
		MIME: application/vnd.in-toto+json
