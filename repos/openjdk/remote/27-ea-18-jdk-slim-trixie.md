## `openjdk:27-ea-18-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:cf673daf5d061d1655a0e2158773d156c27482c7958bf2d20a470ee56a0fb3de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-18-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:f90c1e66f1b9d531433be3dbba9e2424b82179a5b4c3754db676bcc741d841db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260940432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2354e9fc47d969989183a4045db7bd12378701aac15bc0e0300e358655ec9c0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:45:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:45:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 22 Apr 2026 01:45:56 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:45:56 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:45:56 GMT
ENV JAVA_VERSION=27-ea+18
# Wed, 22 Apr 2026 01:45:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 22 Apr 2026 01:45:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973e1dd1ba5f69ff23c36757389c0ac78e18a23d33a6e244157b0ef5118ce82b`  
		Last Modified: Wed, 22 Apr 2026 01:46:16 GMT  
		Size: 2.4 MB (2371160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f2b1dd692c44fa471032c06bfa8be985e51dac6985e7db8bd275b2f11ae559`  
		Last Modified: Wed, 22 Apr 2026 01:46:21 GMT  
		Size: 228.8 MB (228789098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-18-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:faaef991c5ea1622e213e781e6a25cbc12fa9ec343f5beb72b9bc817110bb84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d330c6777b303c094ac1eba6d36d4a9326a2aa6489c1df37c207e8910b4987d2`

```dockerfile
```

-	Layers:
	-	`sha256:1a3b09179632bea75b9887ef87ed44209d21eca74b4646af9f37cd7391941bf1`  
		Last Modified: Wed, 22 Apr 2026 01:46:16 GMT  
		Size: 2.3 MB (2277625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3668e5561cae41de419434725eaaecc59359783358e11f939d0a216ce5e4aced`  
		Last Modified: Wed, 22 Apr 2026 01:46:15 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-18-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:63c2485a23d963763e1a95cd6e3bc9994f7201c4edbedd9ae7f2e5df7cdcfcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259207213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd486ea8e6ea5cbfda98d02146e92350dd4da55b2c142ae152e02f1979a0b36`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:48:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:48:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 22 Apr 2026 01:48:44 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:48:44 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:48:44 GMT
ENV JAVA_VERSION=27-ea+18
# Wed, 22 Apr 2026 01:48:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='d52a5c752f3361d900a611b63a9ac32aa6b5bf98ecccc17bf27f9e8fbc17a042'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/18/GPL/openjdk-27-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6583a52b10083b4851a50d3e066d84f6e986c9fce8b94f12985566ff370382e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 22 Apr 2026 01:48:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ff7929aff2964870610595357a0475cf1c2146f4f8e60280ee9dcdd8c97eb1`  
		Last Modified: Wed, 22 Apr 2026 01:49:04 GMT  
		Size: 2.3 MB (2314380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7288586d44abdc406c391aa0a88fbf03f68f850608d81a1b593f8784c700100`  
		Last Modified: Wed, 22 Apr 2026 01:49:10 GMT  
		Size: 226.7 MB (226749227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-18-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:377956bf680588bf406fc15f40fd079cefc5e78cf0cb4194fe04971663c90f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4393448bed8b1a85e1926337d2f742a4272cc925df5285ef130b0209e61819d`

```dockerfile
```

-	Layers:
	-	`sha256:0ce0eaf61154d59e1fcb5ba3d6228910beb2a12f4cabd79bbe8227e943445ada`  
		Last Modified: Wed, 22 Apr 2026 01:49:04 GMT  
		Size: 2.3 MB (2277311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06f5156c2a16af711b7b26c8f35c9b862446d45003d15e2305868b92807f899d`  
		Last Modified: Wed, 22 Apr 2026 01:49:04 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
