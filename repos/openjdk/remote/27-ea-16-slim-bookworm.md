## `openjdk:27-ea-16-slim-bookworm`

```console
$ docker pull openjdk@sha256:f816faafa21ee66aefb4727ab1cbd97ee2a12eebba2f2f499954feefbe17ac74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-16-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:fb1408a33b839739fcf766c9dfb877da443f2b02dfbd4327b2586ec53ff8011b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261224293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ea159d59b5fb4b86a5b7c39651d3208a18129d719898381a986c208d1b1546`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:02:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:02:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 07 Apr 2026 02:02:59 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:02:59 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:02:59 GMT
ENV JAVA_VERSION=27-ea+16
# Tue, 07 Apr 2026 02:02:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='a9c8f46b87d1c973c4749728845de23d38a1897dc78b85e362f76ce98ca826eb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc96a894335065d7218341881222321567d1eca6950b3d6433fc387295d8d3b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 07 Apr 2026 02:02:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12b7034f2ddbfe94dc496c729f3f6bb99461b6c9789dc39a5987c4ee2d6f1f9`  
		Last Modified: Tue, 07 Apr 2026 02:03:19 GMT  
		Size: 4.0 MB (4029239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7878cca9240825a8ad094b32db0aae7b757eda107c9b6d108381d32f36a066`  
		Last Modified: Tue, 07 Apr 2026 02:03:24 GMT  
		Size: 229.0 MB (228958722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-16-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e9f72be5d60d7a56fb13fd25afb1d6999243928aed5b0b0e811c1aca55cb4ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0de061b4ecab6b3845ebec7854f814daa709176a220eb6c077477d342b297e`

```dockerfile
```

-	Layers:
	-	`sha256:caf2496bb8945e62271a4ccb9da2d92ce770e0f721ea0d9c172d1dc6015b7420`  
		Last Modified: Tue, 07 Apr 2026 02:03:19 GMT  
		Size: 2.6 MB (2649807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:592d0bed2a078d1ab5c8eb1b8bb317aaf7270e6753e116781e748332ec826a56`  
		Last Modified: Tue, 07 Apr 2026 02:03:19 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-16-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4ba61e484525ef428bb20adf379bd93de7c81488a87338b52345ce72032d659b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258891010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca6e495e8d01390c4dbb40c5e01a6ec834d7c67f3fceca215638bce6afc8525`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:05:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:05:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 07 Apr 2026 02:05:57 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:05:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:05:57 GMT
ENV JAVA_VERSION=27-ea+16
# Tue, 07 Apr 2026 02:05:57 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='a9c8f46b87d1c973c4749728845de23d38a1897dc78b85e362f76ce98ca826eb'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc96a894335065d7218341881222321567d1eca6950b3d6433fc387295d8d3b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 07 Apr 2026 02:05:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180d24ef1dbf6b184fe8afc3cbcb4c20c995248959dc8754821274e1f2745d56`  
		Last Modified: Tue, 07 Apr 2026 02:06:18 GMT  
		Size: 3.9 MB (3851931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f0de90c5bca314feaf9dc9a2466aecb98dbdf6b240ce5692aa4d9487bf5473`  
		Last Modified: Tue, 07 Apr 2026 02:06:24 GMT  
		Size: 226.9 MB (226922913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-16-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4d909526ab244fa07ad7507106b1bed401396a69ab743abd7e172f81ee6195e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef5af9e1cb7b0c3c806f585e38366379fdb8517874cf224627c640b6b0ea181`

```dockerfile
```

-	Layers:
	-	`sha256:cdb7b8886e57543142841f9d77445932a16591ad13db7b8ed6ad2d5479c620b1`  
		Last Modified: Tue, 07 Apr 2026 02:06:18 GMT  
		Size: 2.6 MB (2649441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ecb51e3a90e85e56b7012afeb0b01df6fffc41b2f07469d4a9da55adafbb0f1`  
		Last Modified: Tue, 07 Apr 2026 02:06:18 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
