## `openjdk:27-ea-slim-trixie`

```console
$ docker pull openjdk@sha256:06870514c9a372dfe6877edd85a28eb741ded371530919e637472186c2d861aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:e14878a42f684e81591c097926745efad28b531c659dbb7e0e90a1a5811e5127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261122609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5e69e93dd0c3ebd68f95d696455bb5010466ce93490f52e3817560d9a7d952`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:28:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 19 May 2026 23:28:34 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:28:34 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:28:34 GMT
ENV JAVA_VERSION=27-ea+22
# Tue, 19 May 2026 23:28:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 19 May 2026 23:28:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251bbb917959f78ffd903faa42b57cc5c6f72ffd55d29836ec85ab8c01f154a8`  
		Last Modified: Tue, 19 May 2026 23:28:54 GMT  
		Size: 2.4 MB (2371318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ced4245dcb8a2b493e528fe60a494345ca7132fdaae97abedde1149d9eacf`  
		Last Modified: Tue, 19 May 2026 23:28:58 GMT  
		Size: 229.0 MB (228971365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:1f5d660d3c43b1be1de22de148c9dbbe30e1e7b096b0e52523246cb01e9ccdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa065e9335fb7dbd96b23f9d4ddfb3f3b6751be75a0c4268befcdae616a7d4fe`

```dockerfile
```

-	Layers:
	-	`sha256:ec3359710305c929edb5cdfabd363c2aa07c2e94f9cc61474cddae21400ead25`  
		Last Modified: Tue, 19 May 2026 23:28:54 GMT  
		Size: 2.3 MB (2277667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978577c41e4ab1e494c48327b6fb32915c471446069ec6cb1010a3712df673be`  
		Last Modified: Tue, 19 May 2026 23:28:54 GMT  
		Size: 18.1 KB (18107 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3fc7715ef1100724bd036ce7d9fa225115af70936364b149f36c0b8e8f4c8a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259387566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e549c88090ca746518364efb760221e18c9f27441b039b62bb543747964160`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:31:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:32:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 19 May 2026 23:32:13 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:32:13 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:32:13 GMT
ENV JAVA_VERSION=27-ea+22
# Tue, 19 May 2026 23:32:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 19 May 2026 23:32:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6119de0cb83e4dfdda829d247515c338508638e5c8e2e4c4d705226ecc2037`  
		Last Modified: Tue, 19 May 2026 23:32:33 GMT  
		Size: 2.3 MB (2314522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3279934df2181d23d3515a2b0e2ac4f9235b449e299f643dd18cea8bc1e2f980`  
		Last Modified: Tue, 19 May 2026 23:32:37 GMT  
		Size: 226.9 MB (226931125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:42159a93a46fbb7d83cc9ba76d318040695c6d534a7effdecfad876caaf5ed9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7705256a0b8c8fe017066a6a98e3eed69d10b2a952011795f8f1185876c90a49`

```dockerfile
```

-	Layers:
	-	`sha256:d3d2f82c07e17060b002504ad9237ef50bba2434dedddf5e2020dad00d8ac6eb`  
		Last Modified: Tue, 19 May 2026 23:32:33 GMT  
		Size: 2.3 MB (2277345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad801532bdc495b705eb176a1004153b09c0a95424d0b5edf7402c98c009bb7f`  
		Last Modified: Tue, 19 May 2026 23:32:32 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
