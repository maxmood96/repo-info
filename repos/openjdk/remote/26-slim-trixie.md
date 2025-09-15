## `openjdk:26-slim-trixie`

```console
$ docker pull openjdk@sha256:ac5b78a03901f41af2b659d8ecb7e3c5c28fb72de60a22d1267c2bbdb523ffd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:e9f34217e92094bee2896cdb7cf3300649c12e699d041e2d891c4537de83b40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255627120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46a00d2efbcaa65078b6fc2c48fb4c90f4465ec76d7345306a7af63d76821cc`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 12 Sep 2025 18:48:17 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 18:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_VERSION=26-ea+15
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='d8fa7cffcc38d68ed218fa285958e163c48a9b0d5c968c0c8859cc0a36e0baa0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='955e3af91d63b89cb5eecc00503ca439d96a9d2cf645e38e4079ed65c5486ff2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b5e9f324b4221a9921781fc1a9b8f4abe26447236683a8f6c0c53eae3dbca4`  
		Last Modified: Mon, 15 Sep 2025 16:58:03 GMT  
		Size: 2.4 MB (2371149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01115c114463618977763724f19a7c6e0d1ccb862aaf2c00ebf99ab26a632495`  
		Last Modified: Mon, 15 Sep 2025 17:06:51 GMT  
		Size: 223.5 MB (223482476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:aa26622f1e3e0b0156c12048b48d05f2ffb09b3bd503af8284412e615df8a898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d3d4a27ff2aecee8278311dad26d08f4743bf7fb05bdd65375d439ff9d7b70`

```dockerfile
```

-	Layers:
	-	`sha256:9894d416dbb4ee0fd9c050249d6c5cb958b9a57b1e172df46db1d99606c81272`  
		Last Modified: Mon, 15 Sep 2025 18:24:39 GMT  
		Size: 2.3 MB (2282504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1158c0bc6ca8b900254ae1db697fc4561d240d4a69721cb3ae987e6762c6ef0`  
		Last Modified: Mon, 15 Sep 2025 18:24:40 GMT  
		Size: 19.4 KB (19411 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ddc6087edc5688dca712ab30185d0607995088681c61fac98cf0defc9f1bd3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253777457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b76bcae351e0b625e6f5d010ba69af60771cd8b0e3e107a4af9f30907cc32ac`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Fri, 12 Sep 2025 18:48:17 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 18:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 12 Sep 2025 18:48:17 GMT
ENV JAVA_VERSION=26-ea+15
# Fri, 12 Sep 2025 18:48:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='d8fa7cffcc38d68ed218fa285958e163c48a9b0d5c968c0c8859cc0a36e0baa0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/15/GPL/openjdk-26-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='955e3af91d63b89cb5eecc00503ca439d96a9d2cf645e38e4079ed65c5486ff2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Sep 2025 18:48:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20030153787eea34de9b8f92bbfc34bb4e64f387d010f1975a43c86c0115f723`  
		Last Modified: Mon, 15 Sep 2025 16:58:06 GMT  
		Size: 2.3 MB (2314289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bd8de4f119821812b8ff8d2336190164a4ca6d5a31e4516c01868008bb290a`  
		Last Modified: Mon, 15 Sep 2025 17:06:54 GMT  
		Size: 221.3 MB (221326537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:ecce9828d88cddfb7afc503b9cddc45e516363ab695efa42c1b68c1ead04e993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa91ad8b80c1e2071cc13ea459d9ea3be4284e91fdf11bba25293c364925f0a`

```dockerfile
```

-	Layers:
	-	`sha256:964da4089d6ca5ef932f8499af44f3c847250cffe9eddcd3eade1cc773d96086`  
		Last Modified: Mon, 15 Sep 2025 18:24:48 GMT  
		Size: 2.3 MB (2282238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2ee5c740fae2f65f9ac21bee30bcb0843815be115fb3603e02194636a92b0bb`  
		Last Modified: Mon, 15 Sep 2025 18:24:49 GMT  
		Size: 19.6 KB (19626 bytes)  
		MIME: application/vnd.in-toto+json
