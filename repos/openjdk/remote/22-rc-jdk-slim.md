## `openjdk:22-rc-jdk-slim`

```console
$ docker pull openjdk@sha256:5f9a1d407b0cf273b4f2a553db5d67109b8e72f05cb04d0e1199b077438fcabb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-rc-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:cb556e8b3dcec788a71b0e69b9141181d364f4945463ccdb526e0cf262b42678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236070569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f71a6caa12878d0787c00f0e2ea511674f2cb8653d6324b919ee5ecd0997e9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Feb 2024 19:48:24 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 16 Feb 2024 19:48:24 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 19:48:24 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_VERSION=22
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8ea3b5e19b1655d9bed052e9c33c0c075a6009c5f76f96afd42db063f7c6e3`  
		Last Modified: Tue, 12 Mar 2024 01:57:35 GMT  
		Size: 4.0 MB (4014976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc0f00d52f75dd0ffd34673a483356e1e6478ad8cac983c53b1fdd5979c9604`  
		Last Modified: Tue, 12 Mar 2024 01:57:40 GMT  
		Size: 202.9 MB (202931412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:90902aecf783f2fe015613db3cfcf56a5b0cac5ff8e0bd28f2d67372173984ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a3a31cf801ca0a3112f097964e9bb95a187ba31093c2bbe219781631cd5a6b`

```dockerfile
```

-	Layers:
	-	`sha256:e941a3c7d174fbc146189fb1c1fab25eaa7c5256d24c33fb0bc34642d6fa4663`  
		Last Modified: Tue, 12 Mar 2024 01:57:35 GMT  
		Size: 2.3 MB (2346184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824ef75683291533c53ae6ff809e52ad6acd9bbe852a48eb5958a26a2d541455`  
		Last Modified: Tue, 12 Mar 2024 01:57:35 GMT  
		Size: 18.1 KB (18104 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-rc-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f0dd60eb23204056492b92c777150afa62f8d6857057416c8907b9b0327dbee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233971784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1b50575086dae9e05e3ddab936051ca24dcec34f5e2987c602f3831280ab86`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 16 Feb 2024 19:48:24 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 19:48:24 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2024 19:48:24 GMT
ENV JAVA_VERSION=22
# Fri, 16 Feb 2024 19:48:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='4d65cc6ed28711768fd72c2043a7925f7c83f5f51bb64970bd9d52f7791fc6ac'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/36/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='b272e3228d2a3e04b126d54844d33cc6d137256490526cd08679d7023d07d4b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 19:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1e9c7916a6ccf7810e822d985a2f9d022599aef32a11c6676f3590484cf2cd`  
		Last Modified: Wed, 14 Feb 2024 01:16:16 GMT  
		Size: 3.8 MB (3820100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a63a691bb6dc690646d5fca3e87fffabbdcf5c724ce8dd8102a26c8ebcf618`  
		Last Modified: Sun, 18 Feb 2024 05:23:42 GMT  
		Size: 201.0 MB (200995321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:ad6da37125602eb4a42457a917452426486405199f11e656ee3c408c9ca6759e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8c2f7baad09796ccc9a7989287732ae216c76f42f3aaed159b33dc991bf53b`

```dockerfile
```

-	Layers:
	-	`sha256:99bb87ae1f05310291de639487abf24245e04c054a569259d17cab7458ecd0fb`  
		Last Modified: Sun, 18 Feb 2024 05:23:38 GMT  
		Size: 2.3 MB (2346405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6b2b72765b4a7715aa29e8a03f5591f32a090e34b7af7f59faebd3ad3effda1`  
		Last Modified: Sun, 18 Feb 2024 05:23:37 GMT  
		Size: 18.0 KB (17955 bytes)  
		MIME: application/vnd.in-toto+json
