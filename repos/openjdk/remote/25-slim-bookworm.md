## `openjdk:25-slim-bookworm`

```console
$ docker pull openjdk@sha256:34f10f3a1a5b638184ebd1c5c1b4aa4c49616ae3e5c1e845f0ac18c5332b5c6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d72b15406b02e0d5bf82f9cb7ef29c125a037f5d1693a9ef1f23ebbfe47fdb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244080403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f0db4247fb3a478cc33918dcc74114649df9b1a8d825ecca48a0448c0ff4b4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 21 Jan 2025 19:48:21 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_VERSION=25-ea+6
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='bce58f68a52298cfdc57d8beacb469d33408f1d816b22fbf89b22f70efdc9895'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f2895ce0d995d0a063f77d3e3fe7920b22a083b4dc7cba3f85575e93f049a4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b87618fcc5dcd2feb448626958ccc5b9a8b79ec29ba14dc461969e67f0fd4c`  
		Last Modified: Wed, 22 Jan 2025 02:28:29 GMT  
		Size: 4.0 MB (4018362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ed3cb635b4c4c2401ab31efa1e90a3def650466e24247abb13d37c21813729`  
		Last Modified: Wed, 22 Jan 2025 02:28:34 GMT  
		Size: 211.8 MB (211849624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:779465fe05e8ac9641e532decb18b854fd1042d566106fdb8c4c53e1c8557acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6b16fe02f701bfa99870e55094ae3dcf1db3796a8907e397c255168acb5e8e`

```dockerfile
```

-	Layers:
	-	`sha256:a5b8b2206923a551b4babc13d8cd10f755f99c58e2c0d3904c803589ed36e68f`  
		Last Modified: Wed, 22 Jan 2025 02:28:29 GMT  
		Size: 2.5 MB (2533878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:107e6c5059957d77f99c4c2b3ee2f6a69fd597616419a272dd9ba6857da914fb`  
		Last Modified: Wed, 22 Jan 2025 02:28:29 GMT  
		Size: 19.4 KB (19425 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:24048fb8ea972673f146711f9416162e51e4ea7065f2057bd9738c0be1623c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241678576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814dc5fe2d8901ff90f1a272370246d9b8190c7351cfa0e6cdc0b06a8ab117bd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Tue, 21 Jan 2025 19:48:21 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 19:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 19:48:21 GMT
ENV JAVA_VERSION=25-ea+6
# Tue, 21 Jan 2025 19:48:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='bce58f68a52298cfdc57d8beacb469d33408f1d816b22fbf89b22f70efdc9895'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/6/GPL/openjdk-25-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='2f2895ce0d995d0a063f77d3e3fe7920b22a083b4dc7cba3f85575e93f049a4a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 21 Jan 2025 19:48:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f083f07e13bd63cd44a785caf631d4e023799e01a18898c1a673879d76b06aa`  
		Last Modified: Wed, 22 Jan 2025 02:34:57 GMT  
		Size: 3.8 MB (3833715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8987b9edeb7454beca9595dfbfeac861bbbf206f84c1475b3c69ee74aba54f2`  
		Last Modified: Wed, 22 Jan 2025 02:35:02 GMT  
		Size: 209.8 MB (209803830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:9299bfed2941696c9d43d396ffac5b50e8ceca4d904848be0ae2a0c07f32305e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc11de8dee0d626f8d6b70506d269bb2402c96970a2056fe3760f1ea5bc58794`

```dockerfile
```

-	Layers:
	-	`sha256:7cf378ec68c9a02c7a2c8fa911be6bd95d8fa8947d885bfed2b66075b628e4a6`  
		Last Modified: Wed, 22 Jan 2025 02:34:57 GMT  
		Size: 2.5 MB (2533608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4de4112f6314402072b13ada3d6447b633de9122ba496dd0e000aa260cdd0b33`  
		Last Modified: Wed, 22 Jan 2025 02:34:56 GMT  
		Size: 19.6 KB (19640 bytes)  
		MIME: application/vnd.in-toto+json
