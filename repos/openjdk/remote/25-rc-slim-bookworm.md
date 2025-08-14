## `openjdk:25-rc-slim-bookworm`

```console
$ docker pull openjdk@sha256:dc893657480ab8c2249cf39061c5fc52383256ecd51ab406248546f4b49562c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-rc-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:4d041fc68d613b5d6ce6fd2533e2f575f1971207258c0794d4d4570e0a358231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255493308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8b7fd41ea8c60f05aa0fb1ba971a59e05e58e8e27df4893555ac4b586cf24e`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 Aug 2025 00:48:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 09 Aug 2025 00:48:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Aug 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_VERSION=25
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='c00224c25b0b915f4d69929d90e59dfd66e949f79f7437d334248f7789b646f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='2cf9e308cd667a6134865652839a3f7d59a93198a10841cb893f65248d1852d7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290b62fd8816722d1c88b464a3bf8505ffe6dfa3ea28b6ec6592dd28089a5826`  
		Last Modified: Tue, 12 Aug 2025 21:28:29 GMT  
		Size: 4.0 MB (4027215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299709962d786c35aedc2939f19dd6bd4311422f53ebd778a17793bc8b47ebd4`  
		Last Modified: Wed, 13 Aug 2025 01:01:32 GMT  
		Size: 223.2 MB (223235838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:03de9ee4c8b7022f6572e40465e2005366ad4e0f70095981fdb8d7949fcb1a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2670217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e196b6ab058b6eb8219372beccf989fba71ce8024593799538958a34ea52bd73`

```dockerfile
```

-	Layers:
	-	`sha256:599e8b0526858235209a993908ea1095e5ccd21629424846083b7a745b12e3c3`  
		Last Modified: Wed, 13 Aug 2025 00:23:41 GMT  
		Size: 2.7 MB (2652015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6e32677fb9dff103060eec56889bb8c0095a54684f0241e48e48399e4fdff77`  
		Last Modified: Wed, 13 Aug 2025 00:23:42 GMT  
		Size: 18.2 KB (18202 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-rc-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7b822a38eed34029ccdc4ef4964fad10f14e5368e477a98687bedc24394e69b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252954602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707af18c821934869d6cbb0f11ad48872777d1bab88a7657c59d4785deca31f3`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 Aug 2025 00:48:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 09 Aug 2025 00:48:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Aug 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_VERSION=25
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='c00224c25b0b915f4d69929d90e59dfd66e949f79f7437d334248f7789b646f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='2cf9e308cd667a6134865652839a3f7d59a93198a10841cb893f65248d1852d7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9264d93e235056bbba86b53d5e1017f36cfe68b90a121050621f724be3d3805`  
		Last Modified: Wed, 13 Aug 2025 08:32:03 GMT  
		Size: 3.9 MB (3851294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f327c1f41c453443641e371ff690ee2eae781e64817bbcf08bedb1b158f6345`  
		Last Modified: Wed, 13 Aug 2025 09:16:33 GMT  
		Size: 221.0 MB (221021307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:1977cecbd8601c3da392f00475fd59b49e61f9421774c743894d2e08644865be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2667498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7974dcf30a675024cf0314143ade576ab6bc41f60746ff16b9ec28574f639bec`

```dockerfile
```

-	Layers:
	-	`sha256:6c4251af9457e8793ee4634c6ed71deeb8e5bb448db865625ec5faae709e0ed3`  
		Last Modified: Wed, 13 Aug 2025 09:23:27 GMT  
		Size: 2.7 MB (2650413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a913df4fd43ee16889649651c2744d972c6f107a66584b0be5db2e6d98975b`  
		Last Modified: Wed, 13 Aug 2025 09:23:28 GMT  
		Size: 17.1 KB (17085 bytes)  
		MIME: application/vnd.in-toto+json
