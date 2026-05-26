## `openjdk:27-ea-23-slim-trixie`

```console
$ docker pull openjdk@sha256:4facad8f96c098b2ab08be394477dfce0001359f971d7bf38c854fbc9f7c583f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-23-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:ff0796977cc63b8da47b9b527dd0b0c963c5f244822db86a3df412cc9cf58057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261120763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46d87636e9ee49218044aefb8f85b86e2c660158d597f690f198f9e5eed3938`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:09:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:09:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 26 May 2026 19:09:52 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:09:52 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:09:52 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:09:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b7ef4c5d5b31b1da3d1ffaa1101173333c25937f5db7d8b150e7b8a20bd70cb7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='fc322d442a40de5c1b80f1d8340212c8945e424693fca39a8006accd3427bf59'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 26 May 2026 19:09:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c620ff9ed68f756fc5282f1523058a768a5a0034a6e6a43148c79723d30b5703`  
		Last Modified: Tue, 26 May 2026 19:10:10 GMT  
		Size: 2.4 MB (2371328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3fd6e64929accd8d06728055875f1c1a1f1eaf351b38a5eede5ed6c1f9d515`  
		Last Modified: Tue, 26 May 2026 19:10:16 GMT  
		Size: 229.0 MB (228969509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-23-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:8f510189396a4bc279951035db2e87cc5414159b38515c59b481e686b23672bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ceb259cbeaa932bd76f4890ff8050bfb325c84ab8c5f53f5a000bccd703472`

```dockerfile
```

-	Layers:
	-	`sha256:2fcabcc3b286a55ef22c61243bf0d743a3ce68a386373cfaf97e3ab8a1ab2c0b`  
		Last Modified: Tue, 26 May 2026 19:10:10 GMT  
		Size: 2.3 MB (2277671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05df2c634de4c841f3a19f2aa0af1ceb0662455c4a1d31cb212cff46ec705008`  
		Last Modified: Tue, 26 May 2026 19:10:10 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-23-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f4ed8a9b8edae2be335457c44c9fbfec5058f6c856e1dd324adc1e5fa324eaa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259389709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbca8ebebfc0f92105805f8d19f587cc8a73d301763bc94a1a7ae5df2d597bb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 19:11:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 19:11:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 26 May 2026 19:11:43 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:11:43 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:11:43 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:11:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b7ef4c5d5b31b1da3d1ffaa1101173333c25937f5db7d8b150e7b8a20bd70cb7'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='fc322d442a40de5c1b80f1d8340212c8945e424693fca39a8006accd3427bf59'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 26 May 2026 19:11:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba6536bb4067c134f83ed996fa2d4f6a16bd3bd6b0a4cd81e1f7d1cfe666fa2`  
		Last Modified: Tue, 26 May 2026 19:12:03 GMT  
		Size: 2.3 MB (2314565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4795b2acf487cdff840752e0752c64fc24b488423591c2feba2d9b46373b8626`  
		Last Modified: Tue, 26 May 2026 19:12:10 GMT  
		Size: 226.9 MB (226933225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-23-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:b15b35fcbcca2e6fd58e11238774bfff4c7d96548bb97bcc5ab55c5de4ae39f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcecb2d82e5eaa3c0e83485099646d5a8b8e4b036e6a934156073131816eca85`

```dockerfile
```

-	Layers:
	-	`sha256:9e8dff8dbad9ff3c92c45a9eb6b4db632a2233a893d9dfc580d012e88dec55f3`  
		Last Modified: Tue, 26 May 2026 19:12:03 GMT  
		Size: 2.3 MB (2277349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc8cc4118727a13ea609f5d8c8b80837fa6bcaac4a2f604425630c67c28d35ee`  
		Last Modified: Tue, 26 May 2026 19:12:03 GMT  
		Size: 18.3 KB (18275 bytes)  
		MIME: application/vnd.in-toto+json
