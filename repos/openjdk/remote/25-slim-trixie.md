## `openjdk:25-slim-trixie`

```console
$ docker pull openjdk@sha256:90191c4b15648d3b81e112ba067fe525c2fe70cd53f2cc3cb205d8ffcc05e8de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:d61195dece1a084d499d42c2a9d41e69570f6d0165f675ece1a100c2fd8eaf30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255379916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7598765820fbf23934b688d13a75cbeed094b53431d35f3ecb24b2d8d873e0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 12 Aug 2025 17:48:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 17:48:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 12 Aug 2025 17:48:34 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 17:48:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Aug 2025 17:48:34 GMT
ENV JAVA_VERSION=25
# Tue, 12 Aug 2025 17:48:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='c00224c25b0b915f4d69929d90e59dfd66e949f79f7437d334248f7789b646f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='2cf9e308cd667a6134865652839a3f7d59a93198a10841cb893f65248d1852d7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 12 Aug 2025 17:48:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e848807c967e3f231437718b66b16fff195cf9a606ded7003aa7514cc1d1d3`  
		Last Modified: Tue, 12 Aug 2025 23:39:31 GMT  
		Size: 2.4 MB (2371060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a56be35cc94219eab4ce2bb6f0e1ed0c48ac723385eb40950d1e91938eace24`  
		Last Modified: Wed, 13 Aug 2025 00:29:24 GMT  
		Size: 223.2 MB (223235571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:e9905c4594daf2cffa51de638dc7af66bc07f6b9d411323bce9bf44cb5a13ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d79df3d083c97995c70a692584f289265e24c6c869693048074f4a01a759566`

```dockerfile
```

-	Layers:
	-	`sha256:20000aee58b344da57856ab26a8e684e19231c883930dae361effc4c27d90ec8`  
		Last Modified: Wed, 13 Aug 2025 00:23:37 GMT  
		Size: 2.3 MB (2280974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1376327747ecb5631da247907e8827c9740715a475399d384411cadcf9387d`  
		Last Modified: Wed, 13 Aug 2025 00:23:38 GMT  
		Size: 18.2 KB (18176 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:26ea6df1b907f6788d7590818a9c374e99b07074e1537e0163f35a7e41be0996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253483939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26851d0f23f16c4fdd73a70c5403936ca0e24599214c3578f336d72742c8a49`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 12 Aug 2025 17:48:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 17:48:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 12 Aug 2025 17:48:34 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 17:48:34 GMT
ENV LANG=C.UTF-8
# Tue, 12 Aug 2025 17:48:34 GMT
ENV JAVA_VERSION=25
# Tue, 12 Aug 2025 17:48:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='c00224c25b0b915f4d69929d90e59dfd66e949f79f7437d334248f7789b646f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='2cf9e308cd667a6134865652839a3f7d59a93198a10841cb893f65248d1852d7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 12 Aug 2025 17:48:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512919f072a673e9dab75fcb7614cb9cd2c9167ebea194f8f30082ef4e0d0348`  
		Last Modified: Wed, 13 Aug 2025 08:19:57 GMT  
		Size: 2.3 MB (2314200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f152413291589e590f15dcd691f6f0c0c45dfb4567df6be071fb701c6bd89be7`  
		Last Modified: Wed, 13 Aug 2025 10:19:54 GMT  
		Size: 221.0 MB (221033695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:0918b09b45655eed7f830cfafd88272834f9e19e618b9180e0ec003605a81d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7dbf38c7b18a793f46572fc5ca9d71a419b3155fc9c5c5bc92b8415ba1d5656`

```dockerfile
```

-	Layers:
	-	`sha256:0eb68258f8b2a3ef8710697bc5194ecf1c5fed007613a991d4dc92a1f8fa6943`  
		Last Modified: Wed, 13 Aug 2025 09:23:24 GMT  
		Size: 2.3 MB (2280660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75b352c24cc328a406c51bc012b684f7ab6c2960a52c933e38f137402711c62`  
		Last Modified: Wed, 13 Aug 2025 09:23:25 GMT  
		Size: 18.3 KB (18343 bytes)  
		MIME: application/vnd.in-toto+json
