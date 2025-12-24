## `openjdk:26-ea-jdk-slim-trixie`

```console
$ docker pull openjdk@sha256:0af9d317a22027df794cc5b382723c25f86db6f76ba5cc6e0db35c0f24d47d6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:00cf445bf9a5a3314a190f8039c098c1e56703a076c6277812aa8ac2130df248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260155275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50034c66c5da77f3aeb298a4d9013604fd35e463c9c9191f5020c93d53fa7923`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Wed, 24 Dec 2025 05:19:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:19:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Wed, 24 Dec 2025 05:19:40 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:19:40 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 05:19:40 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 05:19:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 05:19:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33059d660e6591aff1f40b2e54ea1455db58a02650a7aa50ada110337cea4c71`  
		Last Modified: Wed, 24 Dec 2025 05:20:09 GMT  
		Size: 2.4 MB (2371061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3070e6a5de506f9569069e5d49a38f57946e99506c91add52b62176945792d`  
		Last Modified: Wed, 24 Dec 2025 05:20:25 GMT  
		Size: 228.0 MB (228007718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:bfaca2e76e8dae98505694ab2295d1cc1372d128f2c6e9f19eeb23e5fa4266fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5197dac9d4d75b8d9ac33ac0efc03d9da03fdf5e453429349a8b8ecc7bab23c8`

```dockerfile
```

-	Layers:
	-	`sha256:5c62dc8ca3d3dcbb9ead0f2ccd36c0062743ccb980f466df988d502f231f0c34`  
		Last Modified: Wed, 24 Dec 2025 07:24:10 GMT  
		Size: 2.3 MB (2278789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5547bb61232d0a60ec68833273929910366bec76a55c499fc0f1220e2c54295`  
		Last Modified: Wed, 24 Dec 2025 07:24:11 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9ac6021b503cc1a6c4b66d1483e9f64b0092204cb8697ab1588573534a692d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258369128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccfd24c99019df2f269ed08bf834c57971b379d9d996af4dd70b2d3539949bd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Wed, 24 Dec 2025 05:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:20:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Wed, 24 Dec 2025 05:20:38 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:20:38 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 05:20:38 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 05:20:38 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 05:20:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4f10552bb3246c34edf7c2e0d8dbf7c36d0dae2189670b912ea6c61db6999b`  
		Last Modified: Wed, 24 Dec 2025 05:21:10 GMT  
		Size: 2.3 MB (2314083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b8984a9c8816c29eb1a2973d4489837b99081f63bf8dc0bea092041329e49f`  
		Last Modified: Wed, 24 Dec 2025 05:21:46 GMT  
		Size: 225.9 MB (225916417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:997dccc7d871065fa5b46c26b981e556c50105eecf62ea0511e3887c817e4d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19df5a8b91ab43fe2f9178f84552d2b8526aa5026d7965007290b3db7983af5`

```dockerfile
```

-	Layers:
	-	`sha256:1df9e54c74e8621e8ff5f6f152f94adee22c4f26a685890d97f4d0250d00df43`  
		Last Modified: Wed, 24 Dec 2025 07:24:17 GMT  
		Size: 2.3 MB (2278475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bd07274140638897239d15545cd9556a2148c34425070a335751c77a631ff7e`  
		Last Modified: Wed, 24 Dec 2025 07:24:18 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
