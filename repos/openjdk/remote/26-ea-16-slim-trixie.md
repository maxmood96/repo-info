## `openjdk:26-ea-16-slim-trixie`

```console
$ docker pull openjdk@sha256:ac99f9f5f77fbd3bd53e6e1e982aa17d17b738163f750fcbe74b5b481895bbeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-16-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:2cdd0fe40ce5a169c6c6bff2b39467d5dee5fd8d2c66324f59ece97fb555e1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255662474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac3664706d4389113e389430d05408f2a93efb201ff22ac057bc581099dc580`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 20 Sep 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Sep 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+16
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='87ee3d9cfd07f66858b6e519b07d2f23375fb1c1827faeebce6580c31045879f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='116ea44265700afbfe2c15b751ef9e34921fa449663ac0dfb439adef9db9c379'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558eded39a4598fb70faebfe5d1d8be823db32d91a8c48c0fed13610e2f19c05`  
		Last Modified: Mon, 22 Sep 2025 23:42:54 GMT  
		Size: 2.4 MB (2371099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473e0f71267c5df4adfa5084fafa0800790dca50bdce04a2b66e77bf9ab5764`  
		Last Modified: Tue, 23 Sep 2025 00:36:02 GMT  
		Size: 223.5 MB (223517880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-16-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:003d17604af07dc1b7468ad53d1df781c0dd6f287194a62bfc4c99271e516dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e029795548a7b3f5f50d5b738d2558bbc24c46dc1c5b6c21fa28c9faa97e7e87`

```dockerfile
```

-	Layers:
	-	`sha256:4df24f16925b2c682a8f466c3bc1d6122334fde9131de017438a2c53f6c3d57e`  
		Last Modified: Tue, 23 Sep 2025 00:24:11 GMT  
		Size: 2.3 MB (2282504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3462dbbf8f7d3dd9d97bc48555c42082187ca98265c1f49cd5f42791e356941e`  
		Last Modified: Tue, 23 Sep 2025 00:24:11 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-16-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4111dfa5a58622438794908a01e95f7e71afa6a1fd43a052b454456c11f0c8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253823353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aae5b5b1d7d180e361c7b4c8655913240bb9ad5255b458cb26a00bbe9b54637`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 20 Sep 2025 00:48:11 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Sep 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+16
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='87ee3d9cfd07f66858b6e519b07d2f23375fb1c1827faeebce6580c31045879f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='116ea44265700afbfe2c15b751ef9e34921fa449663ac0dfb439adef9db9c379'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8555e0e22ecac4b75bae1ac45038fa112b0f6c2dccc608106f5656e5b942e460`  
		Last Modified: Mon, 22 Sep 2025 22:11:59 GMT  
		Size: 2.3 MB (2314300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd6aa990ec6bb8a61d1e129489d3b155ac9973854934d78ab43b82661d1fe2b`  
		Last Modified: Tue, 23 Sep 2025 00:35:54 GMT  
		Size: 221.4 MB (221372422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-16-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:a6a202a4ecfd4c2c7919ce014ba23748517d7958e6f57016c5a2f838d2e3fc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154d2042eb0db3f089c23ebf425f281d638a674c737df23d1b277769b86c6c63`

```dockerfile
```

-	Layers:
	-	`sha256:efd53814b6aef84a954ff224fb886cecfd5b275eacbe157b9d3ee5ee6872b633`  
		Last Modified: Tue, 23 Sep 2025 00:24:15 GMT  
		Size: 2.3 MB (2282238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff262f9216fc8046ce83dd1834c3c2cb962fa6b18d580b562eb4f42f7aa0a510`  
		Last Modified: Tue, 23 Sep 2025 00:24:16 GMT  
		Size: 19.6 KB (19626 bytes)  
		MIME: application/vnd.in-toto+json
