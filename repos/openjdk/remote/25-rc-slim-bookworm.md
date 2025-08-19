## `openjdk:25-rc-slim-bookworm`

```console
$ docker pull openjdk@sha256:42f6485288092261562bd27467508e30a61e62fcfaaea228053d0c235082e3f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-rc-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:931f069804c23eae651b95a79071467004942107f4df3543c683bbe0162a8371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255497329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ad67ccecc87bd7288496ef4e6735637943488f2284e4a77804f28e9a45338f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a19a7bc2ca0860c18a5ee9fa57cb18aa72a25ebe37cf6ca7e72f24df025bf94`  
		Last Modified: Mon, 18 Aug 2025 21:33:28 GMT  
		Size: 4.0 MB (4027259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb258eb39b663d8723789ff1da7574e0ae76f0c75922221ba9e24d5ff404c95a`  
		Last Modified: Mon, 18 Aug 2025 21:33:57 GMT  
		Size: 223.2 MB (223239815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:24779b11fd6fc657abceb0e2c9ebdea1309a83c9c64006b8d4d111ba99f9bcb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2667744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374bb8bd753fdbad45bdf3cf3346e08da54ac08317d451cc45c3cc5477dc24ae`

```dockerfile
```

-	Layers:
	-	`sha256:e444b0bc64b28ca11118dfb8d5d97823f64cf5f0a7a4acda35a37b9d807273a3`  
		Last Modified: Mon, 18 Aug 2025 21:23:51 GMT  
		Size: 2.7 MB (2650779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73fd7e03fbc8cb1a3dacee1d78d9099e26de22057f5297ef88a17392f4fd358c`  
		Last Modified: Mon, 18 Aug 2025 21:23:52 GMT  
		Size: 17.0 KB (16965 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-rc-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1e87101906c8bbf9cc596d500e9667e1b502891e920111d2b1db128e5de8ff9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252957967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4490d953857e1760ac02987f7df549b77f16032e6756bb55dd37711ae792e330`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18619d6149826238e20d8c833bd88d9141048eb6c0b28fbe96d458d21ffae3c4`  
		Last Modified: Mon, 18 Aug 2025 22:25:41 GMT  
		Size: 3.9 MB (3851380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bfb761a66e9de6efb272a67edc3e30ec28ec001867e18cd3d0dea7158d8087`  
		Last Modified: Mon, 18 Aug 2025 22:37:52 GMT  
		Size: 221.0 MB (221024586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ce450af2c3f65ff88d6eec4a0d65bba258f71587e7d8518cf69f990e3818989b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2667496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ef8ce4c9e426dfe9dd807442f3a43f47e232b7ae22ec00c6390040005cf05f`

```dockerfile
```

-	Layers:
	-	`sha256:3d4ddc7918d59633784e31265d294508bc2357cfab52755c9e241c91d73eecb1`  
		Last Modified: Tue, 19 Aug 2025 00:23:46 GMT  
		Size: 2.7 MB (2650413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4e4dac39fd5c88c372c59a7555f01bfd4d9c5c059c136f991f9ca6fb9ce00e4`  
		Last Modified: Tue, 19 Aug 2025 00:23:47 GMT  
		Size: 17.1 KB (17083 bytes)  
		MIME: application/vnd.in-toto+json
